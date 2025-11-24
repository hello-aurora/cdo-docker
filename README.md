# CDO Docker

This is the Dockerfile to build a Docker image for the Climate Data Operators (CDO) software, based on the Node 20, 22 Alpine and Node 20 Bookworm images, it includes the following packages:

- CDO, v2.4.0
- NetCDF, v4.9.2
- EcCodes, v2.34.1
- HDF5, v1.14.3
- Zlib, v1.3.1

## Usage

```bash
FROM jeremybarbet/cdo:20-alpine
# or
FROM jeremybarbet/cdo:22-alpine
# or
FROM jeremybarbet/cdo:20-bookworm
```

## Links

You can find the Docker images at the following link: [jeremybarbet/cdo](https://hub.docker.com/r/jeremybarbet/cdo)

## Build

To build a new tag of the image:

```bash
docker build --platform="linux/amd64" . -t jeremybarbet/cdo:(20|22)-(alpine|bookworm) -f Dockerfile.(20|22)-(alpine|bookworm) [--no-cache] [--progress=plain]
```

To update the image on Docker Hub:

```bash
docker push jeremybarbet/cdo:(20|22)-(alpine|bookworm)
```
