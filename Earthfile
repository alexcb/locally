locally:
    LOCALLY
    RUN echo "this should not be runnable when remotely accessed (unless we add a trusted-repos list)"

safe:
    FROM alpine:latest
    RUN echo this should work

unsafe:
    FROM alpine:latest
    RUN --privileged echo "this also should not be runnable when remotely accessed (unless we add a trusted-repos list)"
