
Visualization of Convolutional Neural Networks
==============================================


<p align="center">
<img src="https://github.com/dhruvjain/CNN-VIS/blob/master/images/new-logo-Vertical.png?raw=true" height="70" width="90" />
<br>
<b><a href="#overview">Overview</a></b>
|
<b><a href="#features">Features</a></b>
|
<b><a href="#requirements">Requirements</a></b>
|
<b><a href="#work-flow">Workflow</a></b>
|
<b><a href="#slides-and-report">Slides and Report</a></b>

</p>

<br>

This is the Project which we did during our internship at <a href="http://cvlab-dresden.de/" target="_blank" rel="noopener">Computer Vision Lab Dresden</a> under the guidance of People at CVLD and CGV.

## Overview

The primary goal is to Visualize interpret the neural nets for a deeper understanding. A better understanding of these models could lead to a more handcrafted design of CNN’s, higher efficiency or better performance as achieved by Zeiler et al. We divided the Visualization tasks into two broad categories: 
* Activation of Filters
* Gradient Based Visualization
Both 2D as well as 3D visualization was performed in each case.

<p align="right"><a href="#top">:arrow_up:</a></p>

## Features

- **2D VISUALIZATION OF ACTIVATION OF FILTERS** run ```python 2d3d-unordered_vis/2Dunordered.py``` to get the 2d output of conv1 layer filters.
- **3D VISUALIZATION OF OUTPUT FROM EACH NEURON** Here the binary output of each of the output of conv1 filters were generated by implementing the code ```2d3d-unordered_vis/layer_output_vox/layer_output_bin.py``` and were visualized using CGV 3D Viewer.
- **Visualizing by ordering** We tried to reorder the output of conv1 layer filters in various ways:

 * The first by performing k-means clustering by taking any one slice of all 96 filters of conv1 layer. 
 * The second was doing PCA on the  similar rows of image slice. The rows are then reordered on the basis of the values of projection on the principal component in increasing order. This can be obtained by running the code ```ordering_layer1/pca_image/kmeans_pca.py```. 
 * Ordering for whole output images instead of rows in a slice from the volume. Here the output images are stacked column wise to form a vector and Principal Component Analysis (PCA) is done on them. The vectors are then reshaped back to images and are reordered accordingly in the volume. This volume of reordered images are visualized using the cgv-viewer. The code to perform this task is ```ordering_layer1/pca_image/pca_image.py```. A sample screenshot of the reordered volume visualization of conv1 layer is shown below:
<p align="center">
<img src="https://github.com/dhruvjain/CNN-VIS/blob/master/images/pca1.png?raw=true" />
</p>


- **Visualization of Gradients** In this method we calculated the gradients of the output of final layer with respect to the filter weights and visualized them as 3D volume. The gradient calculation can
be found at ```gradient/grad_calc.py```  Demo of variation of gradient among images belonging to a reference class, the classifying neuron of this class being the neuron or classification under inspection, a similar class and a dissimilar class can be found here:

* **DEMO:** 

<p align="right"><a href="#top">:arrow_up:</a></p>

## Requirements

* [Caffe](http://caffe.berkeleyvision.org/): We used ```pycaffe``` (caffe interface in python) to perform all the tasks involving CNNs.
* For 3D visualization we used ```CGV 3D viewer``` which is proprietary of the institute


## Work Flow

We follwed the following workflow during the project:
<p align="center">
<img src="https://github.com/dhruvjain/CNN-VIS/blob/master/images/workflow.png?raw=true" />
</p>


<p align="right"><a href="#top">:arrow_up:</a></p>

## Slides and Report
* [Slides] (https://docs.google.com/presentation/d/1ouAYRkvWxoE3Y5vQkI47lZ6qMsE-QltN2yz1yNwd3dE/edit?usp=sharing)


<p align="right"><a href="#top">:arrow_up:</a></p>


