# Yolo v11 for a Custom Dataset Practice

> This is part of Iowa State EE526 HW4

# How to run?
1. Run: `conda env create -f environment.yml` to create environment.
2. Activate conda env: `conda activate EE526`, for more conda tips, see [here](https://github.com/jona1115/documentations/blob/main/conda/condatips.md).
3. Start jupyter notebook:
    - For a local server: `jupyter notebook` (chose this if you are not sure)
    - For a network: `jupyter notebook --ip=0.0.0.0`
    - To kill the server just ctrl+c twice

Tips:
1. If you want jupter notebook to run in the background, you can use `screen`.

# Debugging tips:
1. It complaining about `data.yaml` not found: I think the `!pip install "ultralytics<=8.3.40" supervision` in one of cells in the notebook actually pip installs globally, and not in the conda environment. Conda and pip works together weirdly. 
    - Fix: Read the error message, it points you to a `.config` folder (mine is in `~/.config`) that has an Ultralytics folder with a file inside with a hardcoded path to a dataset. If that path is wrong, I suggest just deleting the Ultralytics folder and rerun the notebook, it will create the Ultralytics folder again with the correct hardcoded path.