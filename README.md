# pyro

![](campfire.png)

`pyro` is a way to work on things in Jupyter notebooks using both Python and R, all inside a reproducible docker container. Provides different docker containers with jupyter and some common installs for Python and R.

- This repo is connected to [DockerHub](https://hub.docker.com/r/zachbogart/pyro)

## Overview
Below is a list of "pyro containers", which are base docker containers available through DockerHub. They include Python and R, along with different combinations of installed packages for each.

***

# Pyro Containers

| Container | Usage | Dockerfile | Python | R | Description
| :---: | :--- | :---: | :---: | :---: | :--- |
| [vanilla](https://github.com/zachbogart/pyro/tree/main/vanilla/) | `FROM zachbogart/pyro:vanilla` | [Dockerfile](https://github.com/zachbogart/pyro/tree/main/vanilla/Dockerfile) | [Pipfile](https://github.com/zachbogart/pyro/tree/main/vanilla/Pipfile) | [RScript](https://github.com/zachbogart/pyro/tree/main/vanilla/install_packages.R) | The basics for Python (np, pd, plt) and R (tidyverse, janitor, readxl, glue). 
| [rhubarb](https://github.com/zachbogart/pyro/tree/main/rhubarb) | `FROM zachbogart/pyro:rhubarb` | [Dockerfile](https://github.com/zachbogart/pyro/tree/main/rhubarb/Dockerfile) | [Pipfile](https://github.com/zachbogart/pyro/tree/main/rhubarb/Pipfile) | [RScript](https://github.com/zachbogart/pyro/tree/main/rhubarb/install_packages.R) | Useful for [tidytuesday](https://github.com/rfordatascience/tidytuesday) work. 
| [vanilla_swirl](https://github.com/zachbogart/pyro/tree/main/vanilla_swirl) | `FROM zachbogart/pyro:vanilla_swirl` | [Dockerfile](https://github.com/zachbogart/pyro/tree/main/vanilla_swirl/Dockerfile) | [Pipfile](https://github.com/zachbogart/pyro/tree/main/vanilla_swirl/Pipfile) | [RScript](https://github.com/zachbogart/pyro/tree/main/vanilla_swirl/install_packages.R) | Copy of `vanilla` with selected nbextentions pre-installed (see bottom of Dockerfile). 

***  

## In the Wild (How do I get started?)
- Learn by doing! See [zachbogart/pyro-template](https://github.com/zachbogart/pyro-template) for an example project that uses a pyro container to work with some data in either Python or R, and saves some simple results. You can use it as a template to make your own repo.
- You can also `docker pull` manually off of [DockerHub](https://hub.docker.com/r/zachbogart/pyro)

## Installing Packages While Running Jupyter in Docker Container
The pyro containers may be missing some package you really crave. It's easy to install them while running a jupyter notebook. You can execute these in a cell:

Python: 
```
pip3 install <MODULE_NAME>
```

R:
```
install.packages("<PACKAGE_NAME>")
```

- Note: since installs are inside docker, they will be ephemeral and will have to be reinstalled when you rerun a container.

***

## Why pyro?

pyro:
- "py" for Python
- "r" for R
- "o" for...um...o's look like containers? I dunno, I thought it was clever.

Made with 💖

***

#### Image Credit
[Campfire](https://thenounproject.com/search/?creator=4129988&q=fire&i=2879653) by [Zach Bogart](https://thenounproject.com/zachbogart/) from [the Noun Project](https://thenounproject.com/)
