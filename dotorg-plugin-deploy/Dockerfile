FROM debian:stable-slim

LABEL "com.github.actions.name"="WordPress Plugin Deploy"
LABEL "com.github.actions.description"="Deploy to the WordPress Plugin Repository"
LABEL "com.github.actions.icon"="upload-cloud"
LABEL "com.github.actions.color"="blue"

LABEL maintainer="Deven Blackburn <deven@makecodenotwar.co>"
LABEL version="1.0.0"
LABEL repository="http://github.com/hkdeven/wordpress-workflow-actions"

RUN apt-get update \
	&& apt-get install -y subversion rsync \
	&& apt-get clean -y \
	&& rm -rf /var/lib/apt/lists/*

COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
