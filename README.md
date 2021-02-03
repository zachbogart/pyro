# Pyrex



This is a way to work on things in Jupyter notebooks using both Python and R, all inside a reproducible docker container. Provides different docker containers with jupyter and some common installs for Python and R.

- This repo is connected to [DockerHub](https://hub.docker.com/r/zachbogart/pyrex)

***

# Containers

| Container | Usage | Dockerfile | Python | R | Description
| :---: | :--- | :---: | :---: | :---: | :--- |
| [vanilla](https://github.com/zachbogart/pyrex/tree/main/vanilla/) | `FROM zachbogart/pyrex:vanilla` | [Dockerfile](https://github.com/zachbogart/pyrex/tree/main/vanilla/Dockerfile) | [Pipfile](https://github.com/zachbogart/pyrex/tree/main/vanilla/Pipfile) | [R Packages](https://github.com/zachbogart/pyrex/tree/main/vanilla/install_packages.R) | The basics for Python and R. 
| [vanilla_swirl](https://github.com/zachbogart/pyrex/tree/main/vanilla_swirl) | `FROM zachbogart/pyrex:vanilla_swirl` | [Dockerfile](https://github.com/zachbogart/pyrex/tree/main/vanilla_swirl/Dockerfile) | [Pipfile](https://github.com/zachbogart/pyrex/tree/main/vanilla_swirl/Pipfile) | [R Packages](https://github.com/zachbogart/pyrex/tree/main/vanilla_swirl/install_packages.R) | Copy of `vanilla` with selected nbextentions pre-installed (see Dockerfile). 

***  

## Example Usage
- See [zachbogart/pyrex-usage-example](https://github.com/zachbogart/pyrex-usage-example) to see an example
- You can also `docker pull` manually off of [DockerHub](https://hub.docker.com/r/zachbogart/pyrex)

## Why pyrex?

Pyrex:
- "Py" for Python
- "r" for R
- "ex" for...executable? I dunno, I thought it was clever

Made with 💖
