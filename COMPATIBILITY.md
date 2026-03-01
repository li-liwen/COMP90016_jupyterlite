# COMP90016 JupyterLite Compatibility

This document maps the old `COMP90016/environment.yml` tools and libraries to JupyterLite support status.

## Supported in JupyterLite (Pyodide target)

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `biopython`
- `plotly`
- `bqplot`
- `ipywidgets`

These are the primary browser-side targets for starter notebooks.

## Verify Per Release (can vary by Pyodide/JupyterLite version)

- `itables`
- `fastcluster`
- `pysam`

These are tested in `notebooks/00_environment_check.ipynb`.

## Not Supported in Browser JupyterLite (native CLI tools)

- `blast`
- `bwa`
- `fastqc`
- `fastqe`
- `iqtree`
- `mlst`
- `prokka`
- `samtools`
- `snp-dists`

These require a native runtime and should remain in Binder or a local conda environment.

## Recommended Workflow Split

- Use JupyterLite for data exploration, plotting, sequence basics, and lightweight analysis.
- Use Binder/local conda for command-line genomics pipelines and binaries.
