# ShinyTensorflowDocker

Docker container for developing Shiny applications with R, RStudio, tensorflow, and the R tensorflow package. Forked from the great EarthLab repository https://hub.docker.com/r/earthlab/r-tensorflow/ and https://github.com/earthlab/dockerfiles

## How to use

Download and run this image using the following commands:

```
docker pull 4quant/shinytf
docker run -i -t 4quant/shinytf /bin/bash
```    

To use Rstudio:

```
docker run -d -p 8787:8787 4quant/shinytf
```

In a web browser, navigate to localhost:8787 (on linux) or on a Mac, substitute the location pointed to by `docker-machine ip default` for `localhost`.
Log in with username: rstudio, password: rstudio.

## Mounting folders

If you want to share a directory between your host machine and the container, use the `-v` flag in your call to `docker run`, as described [here](https://github.com/rocker-org/rocker/wiki/Sharing-files-with-host-machine).
For more information on how to take full advantage of RStudio in this image, see https://github.com/rocker-org/rocker/wiki/Using-the-RStudio-image.

