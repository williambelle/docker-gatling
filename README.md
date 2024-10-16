# Gatling

Docker image for Gatling load testing tool.

## Tags

- [latest][latest]
- [3.10.0][3.10.0]
- [3.9.5][3.9.5], [3.9.4][3.9.4], [3.9.3][3.9.3], [3.9.2][3.9.2], [3.9.1][3.9.1], [3.9.0][3.9.0]
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

[latest]: https://github.com/williambelle/docker-gatling/blob/6be6de56b862cc8158eaaaca80b367dd8b48dcd3/ubuntu/Dockerfile
[3.10.0]: https://github.com/williambelle/docker-gatling/blob/6be6de56b862cc8158eaaaca80b367dd8b48dcd3/ubuntu/Dockerfile
[3.9.5]: https://github.com/williambelle/docker-gatling/blob/14bd33c0a330ec2549526e3a0a5386b405bd3aae/ubuntu/Dockerfile
[3.9.4]: https://github.com/williambelle/docker-gatling/blob/ef02892706e17771e60dea68218efdbe5f24f258/ubuntu/Dockerfile
[3.9.3]: https://github.com/williambelle/docker-gatling/blob/123b918305b02ffc38d05f2d171fcf7d203d7583/ubuntu/Dockerfile
[3.9.2]: https://github.com/williambelle/docker-gatling/blob/78e4f960e3b382ca09fb6428c6ebc3291e14c429/ubuntu/Dockerfile
[3.9.1]: https://github.com/williambelle/docker-gatling/blob/ac360d0699b23e76d29f16b2ee272b314cd686c9/ubuntu/Dockerfile
[3.9.0]: https://github.com/williambelle/docker-gatling/blob/e2ae01c12895838eed400bdbc06d6f687507dccf/ubuntu/Dockerfile
[3.8.4]: https://github.com/williambelle/docker-gatling/blob/a2a7a2ede2d7c4960d99932a1dd4f97cbb6fc9ef/ubuntu/Dockerfile
[3.8.3]: https://github.com/williambelle/docker-gatling/blob/16109ccdc5bd7341d09c4c85d98a902a22e63766/ubuntu/Dockerfile
[3.8.2]: https://github.com/williambelle/docker-gatling/blob/3e039c7fa611d0c467d065f5ab5f62761d3a0692/ubuntu/Dockerfile
