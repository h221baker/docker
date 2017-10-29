## Build docker image

```
docker build -t code_builder:latest --rm .
```

## Create container
```
docker create \
           --name code_builder \
           -v /etc/group:/etc/group:ro \
           -v /etc/passwd:/etc/passwd:ro \
           -u $(id -u hjz):$(id -g hjz) \
           -e USER=hjz \
           -v /home/hjz/Development/aosp/:/aosp/ \
           -t -i code_builder
```

## Start new interactive session
```
docker start -i -a code_builder
```

## Start docker daemon
```
sudo systemctl start docker
```

## Stop docker daemon
```
sudo systemctl stop docker
```
