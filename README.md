# NeRF 

NERF (Neural Radiance Fields) is a method that can synthesize novel 3D views of complex scenes by optimizing an underlying continuous volumetric scene function using a sparse set of input views.

This project is an implementation of NeRF using the [Lego Dataset](https://drive.google.com/drive/folders/1lrDkQanWtTznf48FCaW5lX9ToRdNDF1a)

## Approach

This approach represents a scene using a fully-connected (non-convolution) deep neural network, whose input is a single continuous 5D coordinate (spatial location (x,y,z
) and viewing direction θ,ψ
) and whose output is the volume density and view-dependent emitted radiance at that spatial location.

The views are synthesized by querying 5D coordinates along camera rays and use classic volume rendering techniques to project the output colors and densities into an image. Because volume rendering is naturally differentiable, the only input required to optimize the representation is a set of images with known camera poses.




<p align="center">
  <img src="Assets\procedure.jpg" alt="procedure" width="500"/>
</p>

Please refer to the [Wrapper.ipynb](Wrapper.ipynb) file for implementation details.

## Results
<p align="center">
  <img src="Results\NeRF.gif" alt="NeRF" width="350"/>
</p>

## References
1. [RBE 549: Computer Vision Project 3](https://rbe549.github.io/fall2022/proj/p3/)
2.  Ben Mildenhall, Pratul P. Srinivasan, Matthew Tancik, Jonathan T.
Barron, Ravi Ramamoorthi, Ren Ng, ”NeRF: Representing Scenes as
Neural Radiance Fields for View Synthesis.” [Link](https://arxiv.org/abs/2003.08934)
3. https://towardsdatascience.com/its-nerf-from-nothing-build-a-vanilla-nerf-with-pytorch-7846e4c45666
4. https://colab.research.google.com/github/keras-team/keras-io/blob/master/examples/vision/ipynb/nerf.ipynb
5. https://www.matthewtancik.com/nerf








