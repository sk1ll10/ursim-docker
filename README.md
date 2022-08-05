# ursim-docker

Run Universal Robots Simulator in a docker environment.

Contains Offline Simulator - e-Series - UR Sim for Linux **5.12.2**

https://www.universal-robots.com/download/software-e-series/simulator-linux/offline-simulator-e-series-ur-sim-for-linux-5122/ (behind login wall, download will be done directly via aws in Dockerfile)

## Usage

Tested on Ubuntu 20.04, Docker 20.10.14, docker-compose 1.25.0

### Building the image

```
docker-compose build
```

### Run the Container + application

Atm `install.sh` is invoked at every startup automatically since some commands cannot be executed in the docker build process. The first start installs some stuff, after that startup is fast enough for daily use.

```
docker-compose up
```

Special thx to https://github.com/ljden/URSim_Install_Guides for finding a lot of stuff needed to get this thing running.
