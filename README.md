# Radial Scope plot 
### The matplotlib/rdkit version

You can directly use this code on mybinder (no need to install anything) simply click on the link below, edit the fields with the smiles string of you molecule and `Ctrl+Enter` or click on Run in the toolbar above to execute the cells. 

If you want to install this code locally on your system (e.g to make modifications to the plotting script in `radialscope.py`) follow the instructions below. 

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/duerrsimon/substrate-scope-plot/master?filepath=radial_scope_plot.ipynb)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3591815.svg)](https://doi.org/10.5281/zenodo.3591815)

If you want to cite this code (you do not have to), use the DOI.

#### Orginal idea
This figure made its rounds on twitter based on this tweet https://twitter.com/NarayanLab/status/1206652692321292288

Original credit goes to Attabey Rodríguez Benítez [@ScienceBey](https://twitter.com/ScienceBay) and Alisson Narayan 

This is a completely automated matplotlib version of this plot using RDKit for generating the molecules based on SMILES strings.



### How does it work

1.Get a SMILES string from ChemDraw  or any other software able to output SMILES strings (such as [PubChem](https://pubchem.ncbi.nlm.nih.gov/edit3/index.html).
For every $R_x$ group put a methyl group.
2. Setup the python dictionary for the settings
3. Setup a dictionary for each $R_x$ you want to replace with like the ones shown in the cell below
4. Execute all cells the Run button or Ctrl+Enter

### Installation

Use this within a Python Anaconda distribution, e.g [Miniconda](https://docs.conda.io/en/latest/miniconda.html)
Anaconda is available on Windows, Mac and Linux and this should work on all platforms.

Clone this repo using git

    git clone https://github.com/duerrsimon/substrate-scope-plot.git

Create environment containing rdkit, matplotlib, svgutils

    conda env create -f environment.yml


Then fire up a jupyter-notebook from the terminal like so

    cd substrate-scope-plot
    jupyter-notebook
    
### How does it look like
![radial scope plot example](https://raw.githubusercontent.com/duerrsimon/substrate-scope-plot/master/substrate_scope_replaced.svg?sanitize=true "radial scope plot example")


#### Changelog 
v0.4 | 7.1.2020

- add environment.yml and mybinder links

v0.3 | 30.12.2019

- bug fixes to the colorbar and addition of min_max_value for colorbar

v0.2| 23.12.2019
- put all the plotting in a class that is called from the notebook
- multiple radial scope plots possible 
- correct automatic positioning based on the index of the atom from the SMILES
- addition of rendering of small organic rests (hacky, the user will need to reposition the images using a vector software)
- added some options such as
    - rounding options
    - bw atom theme
    - bold font
    - rounding based on threshold value
- text becomes white at 80% of max value

v0.1 | 17.12.2019
- first rough reproduction of the figure using matplotlib
