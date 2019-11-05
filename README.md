# Docker Images repository

Images at this repo:
- Cherrytree
- Dradis CE

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
           --privileged \
           cherrytree:latest
```

A GUI will popen on the host.

## Run Dradis CE

Create the container

```
docker run --name dradis dradis-ce
```

Browse to ```localhost:3000```