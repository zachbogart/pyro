# pyrex

![](measuring_cup.png)

This is a way to work on things in Jupyter notebooks using both Python and R, all inside a reproducible docker container. Provides different docker containers with jupyter and some common installs for Python and R.

- This repo is connected to [DockerHub](https://hub.docker.com/r/zachbogart/pyrex)

***

# Containers

| Container | Usage | Dockerfile | Python | R | Description
| :---: | :--- | :---: | :---: | :---: | :--- |
| [vanilla](https://github.com/zachbogart/pyrex/tree/main/vanilla/) | `FROM zachbogart/pyrex:vanilla` | [Dockerfile](https://github.com/zachbogart/pyrex/tree/main/vanilla/Dockerfile) | [Pipfile](https://github.com/zachbogart/pyrex/tree/main/vanilla/Pipfile) | [RScript](https://github.com/zachbogart/pyrex/tree/main/vanilla/install_packages.R) | The basics for Python (np, pd, plt) and R (tidyverse, readxl, glue). 
| [vanilla_swirl](https://github.com/zachbogart/pyrex/tree/main/vanilla_swirl) | `FROM zachbogart/pyrex:vanilla_swirl` | [Dockerfile](https://github.com/zachbogart/pyrex/tree/main/vanilla_swirl/Dockerfile) | [Pipfile](https://github.com/zachbogart/pyrex/tree/main/vanilla_swirl/Pipfile) | [RScript](https://github.com/zachbogart/pyrex/tree/main/vanilla_swirl/install_packages.R) | Copy of `vanilla` with selected nbextentions pre-installed (see bottom of Dockerfile). 

***  

## In the Wild
- See [zachbogart/pyrex-usage-example](https://github.com/zachbogart/pyrex-usage-example) to see an example
- You can also `docker pull` manually off of [DockerHub](https://hub.docker.com/r/zachbogart/pyrex)

## Why pyrex?

Pyrex:
- "Py" for Python
- "r" for R
- "ex" for...executable? I dunno, I thought it was clever

Made with 💖

***

#### Image Credit
[Measuring Cup](https://thenounproject.com/zachbogart/collection/strolling-through-the-container-store/?i=3644180) by [Zach Bogart](https://thenounproject.com/zachbogart/) from [the Noun Project](https://thenounproject.com/)