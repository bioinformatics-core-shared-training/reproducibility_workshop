### Computational Reproducibility: Workshop Report ###

#### Introduction ####

  - motivation for reproducibility (cite Florian?)
  - cost/benefit analysis
  - target audience: computational people, wet biologists, funders

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
