# MATLAB scripts tool for Semi-Automatic Lineage Construction

## Installation 

First clone the repo using the command below: 

```git clone https://github.com/abiswas-odu/lineage_track```

### Setup CPD 

1. Open MATLAB and navigate to the code directory called `lineage_track`. Then add the `CPD2` folder and subfolders to PATH. 

2. Then navigate inside the `CPD2` directory and run the command:

```
cpd_make
```

*On MAC OSX you will need to install Xcode from the App store*

## Creating a configuration file

In the test folder you will find an example `config.yaml` file. Make a copy of it into your sample folder and adjust the parameters. 

## Registration 

To run the registration, open `registration\Registration_Centroids.m` or `registration\PrecomputeRegistrationTransforms.m` and point the `config_path` variable to the folder where you have your `config.yaml`.

After registration, to visualize the transforms you can use the script `VisualizeSequence.m`. As before, point the `config_path` variable to the folder where you have your `config.yaml`.

## Tracking 

To perform the lineage tracking, run the script `tree_generation\volume_track_nuclei_divisions.m` with the correct config_file setting. 

## Tree Viz

To visualize the tree, use the script `tree_generation\view_tree.m`

To visualize the tree colored with the intensities, use the script `tree_generation\color_tree.m`
