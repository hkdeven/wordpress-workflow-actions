# WordPress.org Plugin Deploy

This Action commits the contents of your Git tag to the WordPress.org plugin repository using the same tag name. It excludes files in `.git` and `.github` subdirectories and moves anything from a `.wordpress-org` subdirectory to the top-level `assets` directory in Subversion (plugin banners, icons, and screenshots).

## Configuration

### Required secrets
* `SVN_USERNAME`
* `SVN_PASSWORD`

Secrets can be set while editing your workflow or in the repository settings. They cannot be viewed once stored. [GitHub secrets documentation](https://developer.github.com/actions/creating-workflows/storing-secrets/)

### Optional environment variables
* `SLUG` - defaults to the respository name, customizable in case your WordPress repository has a different slug
* `VERSION` - defaults to the tag name; do not recommend setting this except for testing purposes
* `ASSETS_DIR` - defaults to `.wordpress-org`, customizable for other locations of WordPress.org plugin repository-specific assets that belong in the top-level `assets` directory (the one on the same level as `trunk`)

## Example Workflow File
```
workflow "Deploy" {
  resolves = ["WordPress Plugin Deploy"]
  on = "push"
}

# Filter for tag
action "tag" {
    uses = "actions/bin/filter@master"
    args = "tag"
}

action "WordPress Plugin Deploy" {
  needs = ["tag"]
  secrets = ["SVN_PASSWORD", "SVN_USERNAME"]
  env = {
    SLUG = "my-plugin"
  }
}
```

## License

Available for use and remix under the MIT license.
