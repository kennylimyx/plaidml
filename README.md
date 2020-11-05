# Plaidml macOS installation guide

1. Set up environment
Set up a virtual environment using either venv or conda. I prefer conda

For conda, follow these steps:
1. Open terminal
2. type: conda create -n [insert envt name] python=3
3. type: conda activate [inset envt name]

2. Install plaidml (this comes with keras, but not tensorflow
type: pip install plaidml-keras plaidbench

3. Install tensorflow
type: conda install tensorflow

4. Install jupyter
type: conda install jupyter labs

5. Set up plaidml 
type: plaidml-setup
When prompted for experimental devices, type: n
When prompted for graphics card, choose whichever you like (I chose amd_radeon)

6. launch Jupyter notebook 
type: jupyter notebook

7. Import and use plaidml
type: import plaidml.keras
plaidml.keras.install_backend()
import os
os.environ["KERAS_BACKEND"] = "plaidml.keras.backend" 

Once the model is compiled, you should see this:
INFO:plaidml:Opening device "metal_intel(r)_hd_graphics_530.0"

8. Check GPU acitvity using activity monitor
Launch activity monitor
Go to window -> gpu history
