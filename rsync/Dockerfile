FROM debian:stable-slim

LABEL "com.github.actions.name"="rsync"
LABEL "com.github.actions.description"="Copy files using rsync"
LABEL "com.github.actions.icon"="send"
LABEL "com.github.actions.color"="purple"

LABEL "repository"="http://github.com/mthenw/actions"
LABEL "version"="1.0.0"

RUN apt-get update && apt-get install -y \
  openssh-client rsync && \
  rm -Rf /var/lib/apt/lists/*

ADD entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]