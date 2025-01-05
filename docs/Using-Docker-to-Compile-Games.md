## Before You Begin

This guide assumes you are using Ubuntu or one of its derivatives. Some commands might be different if you aren't.

## Setting Up Docker

- Install Docker:

    `sudo apt install docker.io`

- Download the MiyooCFW Toolchain containers:

```
     sudo docker pull miyoocfw/toolchain-shared-uclibc
     sudo docker pull miyoocfw/toolchain-shared-musl
     sudo docker pull miyoocfw/toolchain-static-uclibc
     sudo docker pull miyoocfw/toolchain-static-musl
```

## Compiling apps using docker with MiyooCFW Toolchain:

For e.g. uClibc SDK perform this steps:

```
cd my_game_src_dir/
docker run --volume ./:/src/ -it miyoocfw/toolchain-shared-uclibc:latest
cd /src
make -f Makefile.miyoo
```


## Compiling apps by setting up Project for Docker

- Just outside the project directory, create an empty text file named "make.sh", and add the following text to it, replacing the values of the PROJECT_DIR and MAKE_CMD variables with your project's directory name and compile command (assuming you use shared uClibc SDK):

```
#! /bin/bash

# Project directory (relative, without a trailing slash).
PROJECT_DIR="IOTester"
# Compile command to be run in the container.
MAKE_CMD="make -f Makefile.miyoo zip"

USER_GROUP=`id -gn`
CYAN="\033[1;36m"
NC="\033[0m"

echolog ()
{
	echo -e "\n${CYAN}[INFO]: ${1}${NC}\n"
}

echolog "Creating and starting container..."
CONTAINER_ID=`sudo docker run -v "./${PROJECT_DIR}":"/${PROJECT_DIR}" -itd docker.io/miyoocfw/toolchain-shared-uclibc:latest`

echolog "Compiling in container..."
sudo docker exec -it -w "/${PROJECT_DIR}/" "${CONTAINER_ID}" ${MAKE_CMD}

echolog "Taking ownership of compiled files..."
sudo chown "${USER}":"${USER_GROUP}" "${PROJECT_DIR}"/*

echolog "Stopping container..."
sudo docker stop "${CONTAINER_ID}"
echolog "Deleting container..."
sudo docker rm "${CONTAINER_ID}"
```

- Make the script executable with:

    `chmod +x make.sh`

This script will create a container from the MiyooCFW image, mount your project directory to its filesystem, and leave it running in the background. It will then send the make command to it, fix the ownership of the resulting files, and finally stop and delete the container.

- Compiling Games

    `./make.sh`

The compiled files will be in your project directory.