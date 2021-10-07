# CF-PECO

The correspondence field perturbation based camera arrangement optimization (PECO) algorithm in Matlab.

Submitted to T-PAMI 2021 and based on the paper

<pre><code>@article{Fu2017,
author = {Fu, S. and Safaei, F. and Li, W.},
doi = {10.1109/TIP.2017.2695102},
issn = {10577149},
journal = {IEEE Transactions on Image Processing},
keywords = {Correspondence field,camera optimization,depth estimation,stereo},
number = {6},
title = {{Optimization of camera arrangement using correspondence field to improve depth estimation}},
volume = {26},
year = {2017}
}</code></pre>

## Requirements

Blender >= 2.79

Python >= 2.6

Matlab >=2018a

Install of stereo and optical flow algorihtms from the instruction of the original repostitory:

- SPS-Stereo: Slanted Plane Smoothing Stereo
[spsstereo](https://github.com/siposcsaba89/sps-stereo)

- LIBELAS: Library for Efficient Large-scale Stereo Matching
[libelas](https://github.com/goldbattle/libelas-gpu)

- Stereo matching using adaptive random walk
[open_rwr](https://www.mathworks.com/matlabcentral/fileexchange/49501-stereo-matching-using-adaptive-random-walk)

- Fast Cost-Volume Filtering for Visual Correspondence and Beyond
[Costfilter](https://www.ims.tuwien.ac.at/publications/tuw-202088)

- High accuracy optical flow estimation based on a theory for warping
[OpticalFlow](https://people.csail.mit.edu/celiu/OpticalFlow/)

- FlowNet 2.0: Evolution of Optical Flow Estimation with Deep Networks
[FlowNet](https://github.com/lmb-freiburg/flownet2)


## Install

1. Download the source code.
<pre><code>git clone https://github.com/sf4103154/CF-PECO.git</pre></code>

2. Compile the stereo algorithms based on the pre-mentioned instruction and copy the installed algorithm into 'block_stereomatching' folder under root folder and config the 'stereo.json' file to assign the location of each algoirhtm.

3. Compile the .mex file of the stereo matching algorithm by using matalb in-built compile function.
## Demos

### Synthetic Data

config the config_blender.json file for parameters, specify the scene choosen and the algorithm of stereo matching.

<pre><code> run main_blender_demo.m </pre></code>

### Real Scene Data

config the config_real.json file for parameters, specify the scene choosen and the algorithm of stereo matching.

<pre><code> run main_realscene_demo.m </pre></code>

## Add extra scene data (Optional)
1. create the modeld and save as .blend file
2. attach the <pre><code> viewcapture.py </pre></code> script to the blender srcript tab and save it.
3. put the scene file into <pre><code> \blendermodel</pre></code> folder
4. copy the <pre><code>main_blender_demo.m </pre></code> and change the scene intial camera view variables and scenen range variables (at the top of the .m file) accroding your demand.

## Adjust the PECO algorithm parameters (Optional)
you can change the parameters of the PECO algorithm in the json file <pre><code> peco.json </pre></code> in the root folder.

# License and Citation 
This software and associated documentation files (the "Software"), and the research paper (Improving Stereo Depth Estimation by Perturbation of Angular Orientation of Cameras) including but not limited to the figures, and tables (the "Paper") are provided for academic research purposes only and without any warranty. Any commercial use requires my consent.
