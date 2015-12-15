### Computational Reproducibility: Workshop Report ###
Reproducible Research: A long and winding road.

#### Introduction ####
What do we mean by reproducibility? How do we define it? Why should we strive for it in our research?
  - motivation for reproducibility (cite Florian?)
  - cost/benefit analysis
  Reproducibility does not come for free and , as can be seen later in this paper, can involve considerable effort and a broad skill-base to achieve it. It is therefore reasonable to question - is it worth it?
There is some evidence supporting the concept that papers whose research is reproducible are more highly cited than those which are not.
Greater stability in our confidence in bioinformatic analyses can come from greater robustness of preceding work given how this area of science is so heavily interdependant on derevations from previous annoted data.
  - The target audience of this paper include the folloowing stakeholders: computational scientists, wet biologists and research funders. They have differing roles and rsponsibilities on the road to reproducible research but all are key to the endeavour.

#### Levels of Reproducibility ####

  - computational audit-ability
    - cannot reasonably reproduce, say, ENCODE
    - can leave a sufficiently clear audit/log trail
    - allows for scrutiny of 
  - mechanical reproducibility
    - reproduce figures/tables/numbers from raw data
    - does not imply correctness, but at least can see what was done
    - what duration are we targeting? 5 years? 10 years? 20? 50?  Will your Docker image still be runnable in 50 years?
  - scientific reproducibility
    - arrive at same conclusions via different analysis paths
    - clearly a problem if your result depends on, say, a particular version of some software package
    - not clear what counts as "same conclusions": how much wiggle room is okay?

#### Problem Areas ####

  - versions of software
  - closed-source packages
  - changes in databases and other online resources lead to changes in results
  - assumptions underlying analysis
  - fragile analyses
  - cost of reproducibility, lack of benefits

#### Paths Forward ####

  - funding agencies: have power to dictate change
    - example of open data movement: driven by funders, resisted by journals
    - increase benefits: no repro --> no funding
  - education: many basics are easily taught
    - somewhat harder to convince people that the effort is worth it
  - tools
    - virtualization: Docker, VirtualBox
    - knitr, ipython, etc...
  - robust analysis methods (varied parameters, paired analyses, etc)
