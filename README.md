# Simulation of the beam-beam interaction at LHC during van der Meer scan luminosity calibration

- Please, go to "doc" subdirectory and type "make" to obtain simulation.pdf with the documentation.

- "make" in the main directory compiles "beam_beam" executable from C++ program "beam_beam.C" and runs it over all configuration files of the type beam_beam_\*.txt. An example "beam_beam_cms_4954.txt" is included by default, please, see the comments there for a meaning of all configuration parameters. The results of the simulation are stored in the subdirectories beam_beam_\*. Since we need c++14 compatibility pickup up a late enough CMSSW version, e.g., >=10X.

- "make" in the subdirectory "comparison_with_dynamic_beta_and_deflection_in_R" runs the script "comparison.R" in R programming language for all generated subdirectories beam_beam_\* and produces pdf plots in beam_beam_\*/pdf with the results and the comparison with the old (deflection + dynamic beta) approach. 

[GKK comment: The last step doesn't work for me. Anyway this is simply for plotting. If you are insterested in using R in Ubuntu you can do:
-sudo apt-get install r-base
-in the prompt open R typing `R'
-within R install pacman with install.packages("pacman")
-q() to exit R
-within the comparison_with_dynamic_beta_and_deflection_in_R run `Rscript comparison.R  ../beam_beam_cms_4954`
]
