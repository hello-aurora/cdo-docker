# CDO Docker

This is the Dockerfile to build a Docker image for the Climate Data Operators (CDO) software, based on the Node 20 Alpine image, it includes the following packages:

- Based
- CDO
- NetCDF
- EcCodes
- HDF5
- Zlib

## Usage

To build a new tag of the image:

```bash
docker build --platform="linux/amd64" ./cdo/ -t jeremybarbet/cdo -f cdo/Dockerfile [--no-cache] [--progress=plain]
```

To update the image on Docker Hub:

```bash
docker push jeremybarbet/cdo:latest
```

You can find the Docker image at the following link: [jeremybarbet/cdo](https://hub.docker.com/r/jeremybarbet/cdo)
