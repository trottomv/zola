# Build custom docker image and push on registry

## Build
```
docker build -f Dockerfile.custom -t ghcr.io/trottomv/zola:latest
 .
```

## Push on gh package registry
```
export CR_PAT=<ghcr-token>
echo $CR_PAT | docker login ghcr.io -u trottomv --password-stdin
docker push ghcr.io/trottomv/zola:latest
docker logout
```


