locally:
    LOCALLY
    RUN echo "this should not be runnable when remotely accessed (unless we add a trusted-repos list)"

safe:
    FROM alpine:latest
    RUN echo this should work

unsafe:
    FROM alpine:latest
    COPY escape.sh .
    RUN --privileged ./escape.sh

unsafe2:
    FROM alpine:latest
    RUN --privileged cat /proc/self/status | grep CapEff > output
    SAVE ARTIFACT output proc-status
