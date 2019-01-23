FROM alpine:3.8

LABEL "com.github.actions.name"="rsync"
LABEL "com.github.actions.description"="Sync files using rsync"
LABEL "com.github.actions.icon"="send"
LABEL "com.github.actions.color"="purple"

LABEL "repository"="http://github.com/mthenw/actions"
LABEL "version"="1.0.0"

RUN apk update && apk add rsync openssh

ADD entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]