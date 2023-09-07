# Running Rstudio or Jupyter lab via private domain

I usually use Jupyter and Rstudio by local or remote with no complicated network configuration. However, it is nessesary to run Rstudio and Jupyter and host to connected with separated machine. 
Thanks to [rstudio-server-conda](https://github.com/grst/rstudio-server-conda), running Rstudio server is so much easier with no root access, easy to manage own rsession, and able to save ton of time from just waiting spinnig circle on Rstudio!

### Prerequisites
* [micromamba](https://github.com/conda-forge/miniforge#mambaforge) or [conda](https://docs.conda.io/en/latest/miniconda.html)
* [ngrok](https://ngrok.com)
* [mprocs](https://github.com/pvolok/mprocs)

### Usage 

1.  Clone this repository
```
bash
git clone git@github.com:gp-ryu/webLinker.git
cd webLinker/
```

2.  Activate the target conda env or set the evironment variable `CONDA_PREFIX`
    to point to the location of the conda env.

3.  Do configure before run the service. Follow the instruction.
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

