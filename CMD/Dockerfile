FROM almalinux:8
# it is 1000% same as Centos
RUN yum install nginx -y
RUN echo "hello, welcome to docker" > /usr/share/nginx/hello.html
# daemon off makes our container running and attached to screen
CMD ["nginx", "-g", "daemon off ;"]