FROM arm64v8/alpine:3.8
LABEL maintainer "Wei Gao <wei@gaofamily.org>"

# Install packages
RUN apk --no-cache add bash minidlna tini

# Entrypoint
COPY entrypoint.sh /
ENTRYPOINT ["/sbin/tini", "--", "/entrypoint.sh"]

VOLUME [ "/var/lib/minidlna" ]
