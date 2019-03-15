# CONTRIBUTING

You're awesome!  Here at Allied, we love contributers. :heart_eyes:

<img src="https://media.giphy.com/media/3oxRmq2QcuORRdlKXS/giphy.gif" width="600" />

## GENERAL

Since we're operating on a WordPress platform, [their coding standards][4] will always take precedence.  See style guide below.  

Use [EditorConfig][1] in your editor of choice, whitespace flipping is naughty! :mask:

### Contributing Code

##### Follow these steps:
1.  Open a new or already existing issue
2.  Fork the repo, create a branch, commit your fix
3.  Push the branch, open a pull request
4.  The core team reviews changes, provides feedback if necessary
5.  If fix is approved core team merges the PR
6.  :tada: :tada: :tada:

---

### Development workflow

For small issues like updating a README or other Markdown files, quick pull request or even commit into `master` is acceptable. However, for most new code, we use the [GitHub flow](https://guides.github.com/introduction/flow/):

![GitHub Flow](https://guides.github.com/activities/hello-world/branching.png)

[<img src="https://raw.githubusercontent.com/hkdeven/Be-Constructive/master/top-btn.jpg" align="right"/>][8]

---

## STYLE GUIDE

### JavaScript

Use [WordPress JavaScript Coding Standards][5] as your baseline.

There's too much to list here, but in general we mostly agree with the [Airbnb ES6 style guide][2]] and [Khan Academy React style guide][3] where applicable.

#### Selector naming conventions

Simple words separated by hyphens as a preference to camelCasing or underscores.

### CSS

Use [WordPress CSS Coding Standards][5] as your baseline.

Some suggestions and guidelines that will make the styling codebase simple, readable, consistent and relatively transferable to other CSS processor languages. Approach writing the code with a 'vanilla CSS' ethos, only adding non-standard syntax (SASS or perhaps PostCSS) when absolutely necessary.

#### Nesting

Try to avoid anything more than a selector nested within an already nested selector (three selectors deep).

```scss
.component-name {
  padding: 20px;

  .element {
    font-size: 16px;

    span {
        font-weight: bold;
    }
  }
}
```

#### Media queries

Write media queries at the bottom of the component/page file, each one inside of the main selector name so as to be in scope of the component for component specific variables.

```scss
.component-name {
  /*...*/

  @media screen and (min-width: $breakpoint) {
    /*...*/
  }
}
```

#### Comments

With this approach in mind use CSS comments `/* ... */` and not SASS `//`.

Each CSS file should have the following at the top:

```css
/*
 *  COMPONENT/PAGE NAME
 *  Short description of that component/page
 *
 *  Notes: Anything unusual or complicated to mention
 *  TODO:
 */
```

#### Loops, functions etc

If you really need them, then go bananas ![image](http://www.sherv.net/cm/emo/funny/2/banana.gif) but document extensively.

---

## CODE OF CONDUCT

Above all else, be cool.  Follow the [Open Source Code of Conduct][7].    

:cherry_blossom: :v: :octocat:

[<img src="https://raw.githubusercontent.com/hkdeven/Be-Constructive/master/top-btn.jpg" align="right"/>][8]

---

# ABOUT US

[<img src="https://github.com/hkdeven/AlliedBuildings.com/blob/master/ASB_Logo_Black_Horizontal%202.png?raw=true" align="right"/>][9]

[Allied][9] is a global leader in steel construction, developing solutions for every industry. From aviation to warehouses and everything in between, trust [Allied][9] to be with you all the way. The names and logos for Allied are trademarks of [Allied Steel Buildings, Inc.][9]   

[1]: http://editorconfig.org/
[2]: https://github.com/airbnb/javascript
[3]: https://github.com/Khan/style-guides/blob/master/style/react.md
[4]: https://make.wordpress.org/core/handbook/best-practices/coding-standards/
[5]: https://make.wordpress.org/core/handbook/best-practices/coding-standards/css/
[6]: https://make.wordpress.org/core/handbook/best-practices/coding-standards/javascript/
[7]: http://todogroup.org/opencodeofconduct/
[8]: https://github.com/hkdeven/AlliedBuildings.com/blob/master/CONTRIBUTING.md
[9]: http://alliedbuildings.com/
