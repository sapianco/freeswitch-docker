# freeswitch-docker
Freeswitch Dockerized

# Build Docker image
``` bash
docker buildx build \
    --push --platform linux/arm64/v8,linux/amd64,linux/arm/v7 \
    --build-arg BUILD_DATE=$(date -u +'%Y-%m-%dT%H:%M:%SZ') \
    --build-arg VCS_REF=$(git rev-parse --short HEAD) \
    --tag sapian/freeswitch:latest \
    --tag quay.io/sapian/freeswitch:latest \
    --tag sapian/freeswitch:1.10.7 \
    --tag quay.io/sapian/freeswitch:1.10.7 .
```

