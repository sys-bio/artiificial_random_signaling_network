# artificial_random_signaling_network

## Introduction

The script Ground_truth_generation.jl is to generate the artificial random signaling networks. The SBML files under the folder "data/synthetic_networks.zip" are generated by the Julia script. The SBML files under the folder "data/Biomodels.zip" are signaling networks downloaded from the BioModels Database as a comparison. 

## Citing

If you use any of the codes, please cite the bioRxiv (https://www.biorxiv.org/content/10.1101/2020.05.08.084848) and the GitHub website (https://github.com/SunnyXu/artificial_random_signaling_network).

## Using

To use the Julia script, first install Julia by going to the Julia website (https://julialang.org/). Once you have the Julia console open, make sure you have "RoadRunner" installed by typing `import Pkg` followed by `Pkg.add("RoadRunner")`. RoadRunner.jl is a Julia package for the library of libRoadRunner that is used to provide SBML simulation support. Follow the Julia warnings to install other necessary Julia packages if they have not been installed already.

Next, download the Julia script from Github (https://github.com/SunnyXu/artificial_random_signaling_network/blob/master/Ground_truth_generation.jl) into one folder. At the Julia console type:
`include("pathto\\Ground_truth_generation.jl")`
to run the main script. Note that "pathto" was the path you where you saved the network generation script to, and the double backslash was to avoid the Julia misinterpreting the backslash as a control character. A random signaling network would be generated in SBML format called sampleNetwork0.xml before the steady state and sampleNetwork.xml after the steady state. There were some configuration settings in the Julia script file Ground_truth_generation.jl. These included:

1) The number of species "nSpeces", number of gene species "nSpecies_gene", and number of reactions "nRxns". 
2) Randomly assigned ranges for species concentrations and rate constants could be modified via "rnd_species" and "rnd_parameter".
3) "concentration_perturb" could be used to set the factor that perturbs the concentration at the input species. Default was set to 2.
4) The number of random networks to generate could be set by changing the variable "sampleSize". 

To generate the synthetic networks under the folder synthetic_networks, the Julia script was implemented in Julia 1.6 on Windows 10. 

## Visualization Example

Here is a visualization example by SBcoyote (https://pubmed.ncbi.nlm.nih.gov/37595778/).

<img src="https://raw.githubusercontent.com/SunnyXu/artificial_random_signaling_network/master/visualization_examples/visualization_example.png" width="500" height="400">


