FROM registry.access.redhat.com/ubi8/ubi-minimal:latest

ENV HOME=/opt/scorecard-test \
    USER_NAME=scorecard-test \
    USER_UID=1001

RUN echo "${USER_NAME}:x:${USER_UID}:0:${USER_NAME} user:${HOME}:/sbin/nologin" >> /etc/passwd

WORKDIR ${HOME}

ARG BIN=scorecard-test
COPY $BIN /usr/local/bin/scorecard-test

ENTRYPOINT ["/usr/local/bin/scorecard-test"]

USER ${USER_UID}
