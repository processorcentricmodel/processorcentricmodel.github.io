## Welcome to Processor-Centric Contention-aware Slowdown Model Pages
 
Processor-centric contention-aware slowdown model is a slowdown model for shared memory SoCs. This page includes the code that is used to construct this model. The code is primarily tested on two devices: (1) NVIDIA Jetson Xavier and (2) Qualcomm Snapdragon 855. 

## Introduction & Usage
 
The model construction has two steps. First step is to run all different bandwidth kernels on the target PU under all different external bandwidth demands. The external bandwidth demand is generated by running these kernels on other PUs. The result is recorded as a two-dimensional matrix that each row is the achieved relative speeds of a kernel running on the target processor over different external bandwidth demands (increasingly from left to right). These rows are placed by standalone bandwidth increasingly from top to bottom.
 
The second step is to analyse the above matrix to determine model parameters by running the model construction code.

## Folder Structure 

* corun: The code to generate different bandwidth on processors. 
* model_construction: The code and sample input to construct the model.
 
## Credits
 
The kernel code is inspired by [CS Roofline toolkit](https://bitbucket.org/berkeleylab/cs-roofline-toolkit)
