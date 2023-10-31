### DockerFiles

it is declarative way of creating the images.

we can build the images and we can push to any docker repository

### How to build docker image?

docker build -t <image-name>:version .

FROM: This instruction is used to select base os
RUN: This instruction is used to install or configure inside the base OS and it is executed at the time of image creation
CMD: This instruction will run the container and it is executed at the time of container creation
LABEL: This instruction is used for filtration purpose
