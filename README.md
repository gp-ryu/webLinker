# Running Rstudio or Jupyter lab via private domain

I usually use Jupyter and Rstudio on local or remote with no complicated network configuration. However, it is nessesary to run Rstudio and Jupyter and host it to use under different network schemes.
Thanks to [rstudio-server-conda](https://github.com/grst/rstudio-server-conda), running Rstudio server is now so much easier without needs root access, easy to manage own rsession, and saves ton of time from just waiting spinnig circle on Rstudio!

### Prerequisites
* [micromamba](https://github.com/conda-forge/miniforge#mambaforge) or [conda](https://docs.conda.io/en/latest/miniconda.html)
* [ngrok](https://ngrok.com)
* [mprocs](https://github.com/pvolok/mprocs)
*it automatically installs all prerequisite while doing config anyway...*

### Usage 

1.  Clone this repository
```
bash
git clone git@github.com:gp-ryu/webLinker.git
cd webLinker/
```


2.  Activate the target conda env or set the evironment variable `CONDA_PREFIX`
    to point to the location of the conda env.


3.  Do configure before run the service. You can just follow the instruction to do that.
```
./webLinker config
```


4.  Execute the `webLinker` script with desired service.
```
./webLinker run rstudio -c 16 -m 128G -p 8080
```


5.  Log into service

* open private ngrok at your prefered web browser.
* login with your google account you specified when doing configuration.

### Future features
- [ ] run on HPC
