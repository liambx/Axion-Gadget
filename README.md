# Axion-Gadget
A modifided version of N-body simulation code Gadget2 to perform Fuzzy Dark Matter simulation 

Recently, Fuzzy Dark Matter, motivated by string theory, becomes a popular dark matter candidate among astrophysicists.
Fuzzy Dark Matter has many other names, like Ultra-Light Axion, Scalar Field Dark Matter, Wave Dark Matter etc.
The unique feature of Fuzzy Dark Matter lies in its quantum nature, 
which leads to different equations governing the formation of structures.
This code is modified from the publicly available N-body simulation code Gadget2 (http://wwwmpa.mpa-garching.mpg.de/gadget/).
Gadget2 is the most popular N-body simulation code for cosmological simulation.
In order to put in the new physics in the Fuzzy Dark Matter model, I have modified Gadget2, the theoretical and numerical details
can be found in my paper https://arxiv.org/abs/1611.00892. which is published in ApJ doi:10.3847/1538-4357/aaa485. 
The new paper for cosmological simulation can be found in arxiv:1708.04389, which is also submitted to ApJ.

I am very happy to make my code publicly available, so that other astrophysicists and those who are interested in this topic can
contribute very easily.

Please feel free to use my code and make modifications. Just remember to cite my work, 1611.00892 and 1708.04389 properly, and share this github link.

The new functions are optional in the Makefile, including: 

For turn on the new physics about FDM:               OPT   +=  -DFDM

For testing the calculation about FDM:               OPT   +=  -DFDMTEST (normally no need to turn it on)

For some further correction of FDM:                  OPT   +=  -DFDMBIAS

For testing the further correction:                  OPT   +=  -DFDMBIASTEST (normally no need to turn it on)

For adaptively changin the FDM property:             OPT   +=  -DFDMADAPTIVE (still developing function, not toally mature yet)

For correctly choosing the FDM gravity softening:    OPT   +=  -DFDMGRAVSOFT

For the new functions to be available, the parameter file for starting the simulation is different from original Gadget2.
Please look through the paramter file example carefully, 

here are the new parameters need to be set:

The FDM mass in the unit of 1e-22 eV:                                               FdmAxionMass 2.5

The normalization factor for FDM simulation in the unit of 1e10 solar mass:         FdmNormMass  0.00775466

The size of the kernel chosen for FDM in the unit of kpc:                           FdmKernelLambda 1.414213562

I am still deveping the code and making more consistency test.
If you find any question using the code, please email me: liam_bx@126.com

Zhang Jiajun at The Chinese University of Hong Kong
also at Shanghai Jiao Tong University
