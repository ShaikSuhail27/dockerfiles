ARG version
## ARG variable before FROM will not work after FROM
FROM almalinux:${version:-8}
RUN echo "version is: ${version}"
ARG NAME
ARG COURSE
ENV NAME=${NAME}
# IF WE PASS ARG VARIABLE AS VALUE TO THE ENV VARIABLE THEN IT WILL ALSO WORK AT RUN TIME
ENV COURSE=${COURSE}
RUN echo "My name is ${NAME} and the course is ${COURSE}"