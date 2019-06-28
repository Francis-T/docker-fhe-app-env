# docker-fhe-app-env
This is a template / boilerplate for developing FHE apps over SEAL and HEAAN.

### Pre-requisites ###
You must have Docker installed on your system (regardless of what Operating System).
The particular image used here was built for the x86-64 architecture, so it **might not work** for others (e.g. Raspberry Pi's ARM).

### How to use ###
1. Place your source code in the `app` folder. Everything you put in this folder will be made available to the Docker environment.
2. Run the following Docker command at the top-level directory (i.e. the one containing `app`).
```
docker run -it -v "${PWD}"/app:/app:z francisjt/docker-fhe-env:latest
```
3. You are now inside the Dockerized environment (derived from Debian). Here you can also install whichever utilities and/or libraries you might need through `apt` or by compiling them from source.
4. Using the newly opened terminal, navigate to the `/app` folder and compile your source code.

### How to run the examples ###
#### HEAAN Examples ####
1. Navigate to `app/HEAAN_Examples`
2. Run `make`

#### SEAL Examples ####
1. Navigate to `app/SEAL_Examples`
2. Run `cmake .`
3. Run `make`

