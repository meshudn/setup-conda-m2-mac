1. Install homebrew
2. Download conda forge package from github
https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-arm64.sh
3. Install the package: 
chmod +x ~/Downloads/Miniforge3-MacOSX-arm64.sh
sh ~/Downloads/Miniforge3-MacOSX-arm64.sh
source ~/miniforge3/bin/activate

4. Create a directory and set the python base
conda create --prefix ./env python=3.8
conda activate ./env

5. Install this dependencies for tensorflow
conda install -c apple tensorflow-deps
python -m pip install tensorflow-deps
python -m pip install tensorflow-macos
python -m pip install tensorflow-metal

6. Let's run a script to confirm the installation. Lets install these packages.
conda install jupyter pandas numpy matplotlib scikit-learn

7. Run jupyter notebook
jupyter notebook

8. Run the following code.
import numpy as np
import pandas as pd
import sklearn
import tensorflow as tf
import matplotlib.pyplot as plt
print(tf.config.list_physical_devices())
