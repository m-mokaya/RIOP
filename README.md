Introduction
-------------

This repository contains training data, examples and results reported in https://www.biorxiv.org/content/10.1101/2022.07.15.500218v1. 

Our work is built on previously publised work (REINVENT 3.0 - https://jcheminf.biomedcentral.com/articles/10.1186/s13321-017-0235-x). 

For simplicity, we use a very similar pipeline, therefore you may find it helpful to consult their repository (https://github.com/MolecularAI/Reinvent).


We have provided examples notebooks for creating the input files neccessary to reproduce our results in

```
./notebooks
```


We also provide our datasets for specific experiments where the full Chembl dataset is not used, these are available in 

```
./data
```


Finally, we provide example generated libraries of molecules for each of our experiments in 

```
./results
```

Below is a breakdown of main experiment reported in our work with their experiment index to reference datasets and results. 

| Experiment    | Description |
| -----------   | ----------- |
| 1             | Single property shift     |
| 2             | %-representation       |
| 3             | TPSA shift with rIOP       |
| 4             | QED optimisation with rIOP *      |
| 5             | Generating simple and complex substructures      |
| 6             | Effects of SMILES on model performance       |

*Instructions, examples and tutorials for DrIOP are available at https://github.com/m-mokaya/RIOP_DrIOP

Installation
-------------

1. Install [Conda](https://conda.io/projects/conda/en/latest/index.html)
2. Clone this Git repository
3. Open a shell, and go to the repository and create the Conda environment:
   
        $ conda env create -f reinvent.yml

4. Activate the environment:
   
        $ conda activate reinvent.v3.0

5. Use the tool.
Installation is expected to take a few minutes. 

     
System Requirements
-------------------

* Python 3.7
* Cuda-enabled GPU
* `REINVENT` and `RIOP` have been tested on Linux


Tutorials / `jupyter` notebooks
-----

We have included a series of notebooks that allow show how we did each of our experiments. 

There is another repository containing useful `jupyter` notebooks related to `REINVENT` 
called [ReinventCommunity](https://github.com/MolecularAI/ReinventCommunity). Note, that it uses a
different `conda` environment to execute, so you have to set up a separate environment.


Usage
-----

For concrete examples, you can check out the Jupyter notebook examples in the ReinventCommunity repo.
Running each example will result in a template file.There are templates for many running modes. 
Each running mode can be executed by `python input.py some_running_mode.json` after activating the environment.
    
   Templates can be manually edited before using. The only thing that needs modification for a standard run are the file 
   and folder paths. Most running modes produce logs that can be monitored by `tensorboard`.
