# snakemake-thresholding
Snakemake workflow that uses the Fractal Zarr thresholding module.

# Requirements

* A conda distrubution. Ideally [conda-forge](https://conda-forge.org/) or [miniforge](https://github.com/conda-forge/miniforge), but any will do.

# Installation

Create and activate the environment using the provided `yaml` file.
```bash
conda env create -f configs/conda/environment.yaml
conda activate snakemake-threshold
```

# Usage

Open `configs/parameters.yaml` file and set the path to the image to be thresholded, threshold value and other parameters. Then navigate to the `workflows` directory and execute the Snakefile defining the workflow.
```bash
cd workflows
snakemake --configfile ../configs/parameters.yaml
```

A new layer will appear in your Zarr image. You can use the `notebooks/threshold.ipynb` notebook to check out the results. 
