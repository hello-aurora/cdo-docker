# CDO Docker

This is the Dockerfile to build a Docker image for the Climate Data Operators (CDO) software, based on the Node 20, 22, 24 Alpine and Node 20 Bookworm images, it includes the following packages:

- CDO, v2.4.4
- EcCodes, v2.34.1
- NetCDF, v4.9.2
- HDF5, v1.14.3
- Zlib, v1.3.1

## Usage

### Alpine images

```bash
FROM jeremybarbet/cdo:20-alpine
# or
FROM jeremybarbet/cdo:22-alpine
# or
FROM jeremybarbet/cdo:24-alpine
```

### Bookworm images

```bash
FROM jeremybarbet/cdo:20-bookworm
```

## Links

You can find the Docker images at the following link: [jeremybarbet/cdo](https://hub.docker.com/r/jeremybarbet/cdo)

## Build and push

To build a new tag of the image and push to Docker Hub:

### Alpine images

```bash
docker build --platform="linux/amd64" -f Dockerfile.X-alpine -t jeremybarbet/cdo:X-alpine .
docker push jeremybarbet/cdo:X-alpine
```
### Bookworm images

```bash
docker build --platform="linux/amd64" -f Dockerfile.X-bookworm -t jeremybarbet/cdo:X-bookworm .
```
