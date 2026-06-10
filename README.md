# Manchester Neural Data Analysis Workshop - SpikeInterface

This is the github repo for the SpikeInterface sessions of the Neural Data Analysis Workshop at The University of Manchester.

Please read this page and try to install the software BEFORE the workshop. It will make life easier for everyone.

There will be two SpikeInterface sessions. The first will be a theoretical overview of spike sorting and an introdution to what SpikeInterface is. At the end of this session, we will try and ensure that everyone can get some version of SpikeInterface installed on their machine. Note: if you'd like to try the software out, please bring your own laptop/system!

The second will be a "classroom-style" workshop where you will play with real data. You can either bring your own ephys data, or use openly available data from DANDI, described below. To create a Python environment which will allow you to do some spike sorting, follow the **Install** instructions below.

# Install

First, go to a folder you'd like to keep the code from this repository in. Open this folder in terminal. In terminal, copy (clone) this repo from GitHub then **c**hange **d**irectory into it by running

```
git clone https://github.com/chrishalcrow/manchester_neural_data_analysis.git
cd manchester_neural_data_analysis
```

## uv

I recommend installing [`uv`](https://docs.astral.sh/uv/getting-started/installation/). If you've installed `uv`, make sure you're in the `manchester_neural_data_analysis`. The next command might take a minute to run: it will install all the Python packages we need:

```
uv run test_install.py
```

You should see a successful message with no errors. If that works, you are ready for the workshop.

If you'd like, you can now run the workshop jupyter notebook by running

```
uv run jupyter notebook spikeinterface.ipynb
```

This command should open a web browser with a Jupyter Notebook in it.

## not uv

`uv` is amazing! But if you insist, you can use normal virtual environments. Just `pip install .` from inside `manchester_neural_data_analysis` when you're venv is activate.

# Data

I will explore a couple of `SortingAnalyzer` objects using SpikeInterface-GUI. If you'd like to follow along interactively, please download the files in this Zenodo repository: 

If you have some ephys data you'd like to spike sort, please bring it on the device you are going to use. I believe you'll get the most out of the workshop by trying to run SpikeInterface on your own data.

If you do not have your own data, please download some from DANDI (alternatively, you can _stream_ the data from DANDI, although this will be very very slow). The notebook in this repo uses the data here: https://dandiarchive.org/dandiset/000939/0.260512.1701/files?location=sub-A3702 This is a 2 hour recording from a Cambridge Neurotech probe from Manchester's very own Adrian Duszkiewicz. It's quite big: 23GB!

Here is what my `data` folder looks like:

< image coming soon... >

If you'd like to try a different type of data, you could try:

- IBL Neuropixels 1 data. NOTE: One file is aroud 100GB large. E.g. on of the "ecephys" files https://dandiarchive.org/dandiset/000409/0.260309.1324/files?location=sub-CSH-ZAD-011&page=1
