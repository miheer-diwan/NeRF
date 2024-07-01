# NeRF (Neural Radiance Field)

Neural Radiance Field is a generative model of sorts,
conditioned on a collection of images and accurate poses (e.g.
position and rotation), that allows you to generate new views
of a 3D scene shared by the images, a process often referred
to as “novel view synthesis.” In simple words, NeRF renders
a new view of an object when given some input views. 

This project is an implementation of NeRF using the lego data for NeRF from the original author’s link [here](https://drive.google.com/drive/folders/1lrDkQanWtTznf48FCaW5lX9ToRdNDF1a).

### Approach

The basic NeRF approach represents a scene using a fully-connected (non-convolution) deep neural network, whose input
is a single continuous 5D coordinate (spatial location (x,y,z)
and viewing direction θ, ψ) and whose output is the volume
density and view-dependent emitted radiance at that spatial
location. 
<p align="center">
  <img src="Assets\procedure.jpg" alt="procedure" width="500"/>
</p>

The implementation code is given in Wrapper.ipynb.

### Results
<p align="center">
  <img src="Results\NeRF.gif" alt="NeRF" width="350"/>
</p>

### References
1. https://rbe549.github.io/spring2023/hw/hw0/
2.  Ben Mildenhall, Pratul P. Srinivasan, Matthew Tancik, Jonathan T.
Barron, Ravi Ramamoorthi, Ren Ng, ”NeRF: Representing Scenes as
Neural Radiance Fields for View Synthesis.” [link](https://arxiv.org/abs/2003.08934)
3. https://towardsdatascience.com/its-nerf-from-nothing-build-a-vanilla-nerf-with-pytorch-7846e4c45666
4. https://colab.research.google.com/github/keras-team/keras-io/blob/master/examples/vision/ipynb/nerf.ipynb
5. https://www.matthewtancik.com/nerf








