# Tutorial on using GANs for finding probabilistic solutions to an ill-posed inverse problem  

_Lukas Mosser - 2022_
---
### [Curvenote Page Rendered Here](https://l_moss-tutorial.curve.space/)

## Description

A short tutorial on using a GAN to find solutions to an ill-posed inverse problem.

The inverse problem is taken from the CT-imaging field and uses a radon transform to emulate imaging in a CT-scan. 

The code for the forward problem is provided through the library [torch-radon](). 
This library also allows for computing a gradient of the likelihood with respect to the underlying image.

The image space is represented by a pre-trained GAN, either from MNIST or the Channels dataset. 

The solutions found here are not Bayesian as we find different solutions around the MAP using a gradient-based approach. 

Nevertheless, the tutorial aims to give a self-contained example of how to combine a GAN with a forward problem to find solutions to an ill-posed inverse problem.

The examples with either alot of noise, or few projections do not allow for the geometry of the ground truth number or channel system to be determined. 
The solutions obtained will then have a variety of solutions as many different geometries maximize the a-posteriori probability.

Try it out here: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LukasMosser/tutorial_gans_for_inverse_problems/blob/main/notebooks/Solving_Inverse_Problems_with_Pretrained_Latent_Variable_Models.ipynb)
