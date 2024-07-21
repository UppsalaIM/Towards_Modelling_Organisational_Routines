# Towards_Modelling_Organisational_Routines
Source code and data for the paper "Towards Modelling and Simulation of Organisational Routines".

## Setup

Python requirements can be found in `requirements.txt`. 

To run the data extraction, you will need a [GitHub access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens). 

## Usage

There are three Jupyter notebooks:
* `notebooks/01-Data_Extraction.ipynb` : Loads data from the GitHub REST API. (note: data can already be found in `data/data.xlsx`).

* `notebooks/02-Data_Analysis.ipynb` : Loads `data/data.xlsx` and applies some pre-processing before loading into routines data model objects. It then extracts recurrent action patterns and builds a summary statistics table about the patterns to `data/summary.xlsx`. Finally, a state transition matrix is calculated and output to `data/transition_matrix.xlsx`.

* `notebooks/03-Plot_Figures.ipynb` : Renders the routines data model class diagram from a PlantUML description in `figures/routines_model.txt` as an image output to `figures/routines_model.png` (Fig. 1), then loads `data/summary.xlsx` and `data/transition_matrix.xlsx` to generate respective LaTeX tables (Tables 4 and 5). The transition matrix is then used to plot a visualisation of the Markov chain that is output to `figures/markov_chain_plot.pdf` (Fig. 2).
