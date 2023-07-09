# nanopore-analysis
Jupyter notebook for analysing nanopore sequencing of nanobodies

## Setup
Copy data from the minion computer. Results are stored in Var/Lib/Minknow/Data.

If you have a windows computer then you will need a virtual Ubuntu container to run this analysis. Follow the instructions below.

#### Install Docker Desktop

Download from: https://www.docker.com/products/docker-desktop/

#### Start Ubuntu container in the CMD:

`docker run -ti --rm ubuntu /bin/bash`

The following tools must all be installed inside this Ubuntu container.

#### Install Guppy

Download from: https://community.nanoporetech.com/downloads

#### Install medaka

https://github.com/nanoporetech/medaka

`pip install medaka`

#### Install python

```
apt update
apt-get install python3
```

Check it is installed:

`python3 --version`

#### Install R

`apt-get install -y r-base`

Check it is installed:

`R --version`

Open R and install ggplot2 and patchwork

```
R
install.packages('ggplot2')
install.packages('patchwork')
```

#### Install jupyter notebook and launch nanopore analysis

```
pip install notebook
jupyter notebook Nanopore_Analysis_Template.ipynb
```

#### Save the docker container

To save the container, on the CMD run:

`docker commit <container ID> <name of image>`

To run the image, on the CMD run:

`docker run -dit <name of image>`
