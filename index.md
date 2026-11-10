---
layout: default
---

## About me

**Name:** Zhixiang Zhang

**UCSD email:** [zhz194@ucsd.edu](mailto:zhz194@ucsd.edu)

**Section:** D32

**Mentor:** Yusu Wang

## Project reflections

**What is the most interesting topic covered in your domain this quarter?**

The one that interests me the most is guidance without classifiers and the way it influences the output images of the diffusion model. In Quarter 1 experiments, more guidance tended to make the class easier to distinguish, but it was not always beneficial for the quality of the output images. There were cases where the generated sample had exaggerated colors or thicker digit strokes. The other thing I found useful to consider was denoising trajectory which allowed me to see when the recognizable structure emerges.

**Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

Another area for study could be testing out the effect of using dynamic guidance strength versus the effect of a constant weight on sampling performance. My plan here is to compare the performance of constant guidance against simpler policies which use more strength in guidance while sampling in particular noise bands. To start with, I will run my experiments on MNIST data and expand them onto CIFAR-10 data if there is time left. In all cases, I will use the same starting noise, model, and budget for sampling. The results will include the metrics of requested-label accuracy, distribution similarity, within-class variance, and paired images grid.

**What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

In terms of my comparison of models that have been trained on various datasets of different sizes, there are some ways in which I would like to do things better. For instance, my present approach where I conduct 100-images and 1,000-images experiments using the same amount of training iterations means that each individual image in the smaller dataset will be presented much more times than those from the larger one. This may make it difficult for me to distinguish between the two factors. I would do the matched exposure as well as random seed repetitions in addition to comparing checkpoints.

**What other techniques would you be interested in using in your project?**

Activation steering is another technique for controlling diffusion models that I would like to study. It involves making slight modifications to certain chosen activations at different stages of the process, apart from changing only the mixture of conditional and unconditional predictions. I would begin with a very simple target and test it against classifier-free guidance. In addition, I would like to employ feature space nearest neighbor analysis, in conjunction with the pixel distance measures used in my current research. These would help me assess whether the modification leads to better control without sacrificing diversity.