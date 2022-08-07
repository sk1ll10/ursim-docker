# ursim-docker

Run Universal Robots Simulator in a docker environment using a 16.04 ubuntu base image.

Contains Offline Simulator - e-Series - UR Sim for Linux **5.12.2**

https://www.universal-robots.com/download/software-e-series/simulator-linux/offline-simulator-e-series-ur-sim-for-linux-5122/ (behind login wall, download will be done directly via unprotected aws link in Dockerfile)

*Disclaimer: this software comes without warranty or support. The install process is pretty messy which is @UR's responsibility to fix. Until then this is at least a version that should work out of the box for most people*

## Usage

Tested on Ubuntu 20.04, Docker 20.10.14, docker-compose 1.25.0

### Building the image

```
docker-compose build
```

### Run the Container + application

Atm `install.sh` is invoked at every startup automatically since some commands cannot be executed in the docker build process. I have a stripped down version in the build process `install_copy.sh` which does the heavy stuff so startup using the below command should be fast enough for daily use.

```
docker-compose up
```

Special thx to https://github.com/ljden/URSim_Install_Guides for finding a lot of stuff needed to get this thing running.
