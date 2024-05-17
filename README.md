# Gatling

Docker image for Gatling load testing tool.

## Tags

- [latest][latest]
- [3.9.0][3.9.0]
- [3.8.4][3.8.4], [3.8.3][3.8.3], [3.8.2][3.8.2]

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

[latest]: https://github.com/williambelle/docker-gatling/blob/e2ae01c12895838eed400bdbc06d6f687507dccf/ubuntu/Dockerfile
[3.9.0]: https://github.com/williambelle/docker-gatling/blob/e2ae01c12895838eed400bdbc06d6f687507dccf/ubuntu/Dockerfile
[3.8.4]: https://github.com/williambelle/docker-gatling/blob/a2a7a2ede2d7c4960d99932a1dd4f97cbb6fc9ef/ubuntu/Dockerfile
[3.8.3]: https://github.com/williambelle/docker-gatling/blob/16109ccdc5bd7341d09c4c85d98a902a22e63766/ubuntu/Dockerfile
[3.8.2]: https://github.com/williambelle/docker-gatling/blob/3e039c7fa611d0c467d065f5ab5f62761d3a0692/ubuntu/Dockerfile
