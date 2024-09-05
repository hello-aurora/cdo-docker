# CDO Docker

This is the Dockerfile to build a Docker image for the Climate Data Operators (CDO) software, based on the Node 20 Alpine and Node 20 Bookworm images, it includes the following packages:

- CDO
- NetCDF
- EcCodes
- HDF5
- Zlib

## Usage

To build a new tag of the image:

```bash
docker build --platform="linux/amd64" . -t jeremybarbet/cdo:20-(alpine|bookworm) -f Dockerfile.20-(alpine|bookworm) [--no-cache] [--progress=plain]
```

To update the image on Docker Hub:

```bash
docker push jeremybarbet/cdo:20-(alpine|bookworm)
```

You can find the Docker image at the following link: [jeremybarbet/cdo](https://hub.docker.com/r/jeremybarbet/cdo)
