### DockerFiles

it is declarative way of creating the images.

we can build the images and we can push to any docker repository

### How to build docker image?

docker build -t <image-name>:version .

FROM: This instruction is used to select base os

RUN: This instruction is used to install or configure inside the base OS and it is executed at the time of image creation

CMD: This instruction will run the container and it is executed at the time of container creation

LABEL: This instruction is used for filtration purpose
docker inspect <image-id>--> to check the labels
docker images --filter label=key=value--> for filtering the images

EXPOSE: This instructon is used to tell the user that which port it is opening and it is just providing the information and not providing any functionality.

ENV: This instruction is used for environment variables

COPY: This instruction is used for copy the files to image and the file should present in the current directory where dockerfile exists

ADD: This instruction is also same as copy like copying the files from current directory to the container but it is having two extra capabilities
1.it can directly get the content from internet and will copy 
2.it can directly untar the files 

ENTRYPOINT: this instruction is same as CMD command but this will not be overriden by any command, but CMD can be overridden by any command
Entry point cannot be overriden by any command but the command can append to the entrypoint
if entry point is not passing any argument, then CMD will supply the argument so better to use both CMD and ENtry point for best results

USER:This instruction is used to create user , by default docker will get the root acess to the underlined server and that is not the best practice so we are creating the user

WORKDIR:  this instruction will act as cd(change directory)

##### Docker file push process to docher hub
1.Need to login to docker hub in the server using docker login command and need to enter credentials

Format: docker push <URL>/<user-name>/<image-name>:<version>

