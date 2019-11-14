# Docker Images repository

Images at this repo:
- Cherrytree
- Dradis CE
- Ghidra

## Run ghidra
First allow remote X connections
```
xhost +
```

Create container
```
docker run --name ghidra \
           --rm \
           -v ~/PROJECT_DATA:/root/ \
           --net=host \
           egonzalez90/ghidra:latest
```
## Run Cherrytree

First allow remote X connections
```
xhost +
```

Create the container, LOCAL_CONFIG_DATA is the path where you cherrytree files are located.
```
docker run --name cherrytree \
           --rm \
           -v ~/LOCAL_CONFIG_DATA:/root/ \
           --net=host \
           egonzalez90/cherrytree:latest
```

A GUI will popen on the host.

## Run Dradis CE

Create the container

```
docker run --name dradis egonzalez90/dradis-ce:latest
```

Browse to ```localhost:3000```