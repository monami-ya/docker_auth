FROM golang:onbuild
EXPOSE 5001
VOLUME /config
ENTRYPOINT ["/go/bin/auth_server"]
CMD ["/config/auth_config.yml"]
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && \
    apt-get upgrade -y ca-certificates && \
    update-ca-certificates && \
    apt-get autoremove -y ca-certificates && \
    apt-get clean -y
