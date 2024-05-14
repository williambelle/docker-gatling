# Gatling

Docker image for Gatling load testing tool.

## Tags

- [latest](https://github.com/williambelle/docker-gatling/blob/main/ubuntu/Dockerfile)
- [3.8.2](https://github.com/williambelle/docker-gatling/blob/main/ubuntu/Dockerfile)

## Usage

Pull image:

```sh
# Latest version
docker pull williambelle/gatling:latest

# Specific version
docker pull williambelle/gatling:3.8.2
```

Run container:

```sh
# Simple
docker run -it --rm williambelle/gatling

# With configuration and simulation files from the host
docker run -it --rm \
  -v ./conf:/home/gatling/gatling/conf \
  -v ./user-files:/home/gatling/gatling/user-files \
  -v ./results:/home/gatling/gatling/results \
  williambelle/gatling
```
