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
