# ursim-docker

Run Universal Robots Simulator in a docker environment.

Contains Offline Simulator - e-Series - UR Sim for Linux **5.12.2**

https://www.universal-robots.com/download/software-e-series/simulator-linux/offline-simulator-e-series-ur-sim-for-linux-5122/ (behind login wall, download will be done directly via aws in Dockerfile)

## Usage

Tested on Ubuntu 20.04, Docker 20.10.14, docker-compose 1.25.0

### Building the image

      docker-compose build

### Run the Container + application

Atm `install.sh` has to be invoced manually on the first start due to some `xterm` commands that cannot be executed in the build process. This command can be ommitted in future runs. 

```
docker-compose up -d
docker exec -it ur-sim bash
./install.sh
./start-ursim.sh
```

Special thx to https://github.com/ljden/URSim_Install_Guides for finding a lot of stuff needed to get this thing running.
