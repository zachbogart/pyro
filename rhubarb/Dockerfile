# installing things from scratch through ubuntu

FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

# Python
RUN apt-get update -qq && apt-get -y --no-install-recommends install \
    python3-pip \
    python3-setuptools \
    python3-dev

# pipenv
RUN pip3 install pipenv

# R
RUN apt-get update -qq && apt-get -y --no-install-recommends install \
    r-base \
    r-base-dev 

## install debian packages (for tidyverse import)
# from https://www.r-bloggers.com/2019/02/running-your-r-script-in-docker/
RUN apt-get update -qq && apt-get -y --no-install-recommends install \
    libxml2-dev \
    libcairo2-dev \
    libsqlite3-dev \
    libmariadbd-dev \
    libpq-dev \
    libssh2-1-dev \
    unixodbc-dev \
    libcurl4-openssl-dev \
    libssl-dev

# R's X11 runtime dependencies
# from https://github.com/rocker-org/rocker-versioned/blob/master/X11/Dockerfile
RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    libx11-6 \
    libxss1 \
    libxt6 \
    libxext6 \
    libsm6 \
    libice6 \
    xdg-utils \
  && rm -rf /var/lib/apt/lists/*

# define project directory and move everything over
ENV PROJECT_DIR /project
WORKDIR ${PROJECT_DIR}
COPY . ${PROJECT_DIR}/

# install python modules
RUN pipenv install --system --deploy

# install R packages
RUN Rscript install_packages.R

# install JS/CSS files for jupyter_contrib_nbextensions
RUN jupyter contrib nbextension install --user
