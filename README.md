# Pyrex

This is a way to work on things in Jupyter notebooks using both Python and R, all inside a reproducible docker container. Provides different docker containers with jupyter and some common installs for Python and R.

- This repo is connected to [DockerHub](https://hub.docker.com/r/zachbogart/pyrex)

***

# Containers

| Container | Usage | Dockerfile | Python | R | Description
| :---: | :--- | :---: | :---: | :---: | :--- |
| [classic](https://github.com/zachbogart/pyrex/tree/main/classic/) | `FROM devperiscopic/pyrex:classic` | [Dockerfile](https://github.com/zachbogart/pyrex/tree/main/classic/Dockerfile) | [Pipfile](https://github.com/zachbogart/pyrex/tree/main/classic/Pipfile) | [R Packages](https://github.com/zachbogart/pyrex/tree/main/classic/install_packages.R) | The basics for Python and R. 
| [prepared](https://github.com/zachbogart/pyrex/tree/main/prepared) | `FROM devperiscopic/pyrex:prepared` | [Dockerfile](https://github.com/zachbogart/pyrex/tree/main/prepared/Dockerfile) | [Pipfile](https://github.com/zachbogart/pyrex/tree/main/prepared/Pipfile) | [R Packages](https://github.com/zachbogart/pyrex/tree/main/prepared/install_packages.R) | Copy of `classic` with selected nbextentions pre-installed. 

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
