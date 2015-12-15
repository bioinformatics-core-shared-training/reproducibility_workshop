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

  - versions of software. Programs by their very nature evolve and develop with new features and different libraries being developed and used. Whilst this is great as far as developing new features and capabilities, it comes at the cost of potentially wrecking backwards compatibility with previous versions and delivering different results.
  - It is extremely important for software authors/package maintainers to be scrupulous in documenting changes occurring in new releases of packages, especially if it may break reproducibility.
  - closed-source packages. Versioning can cause ven bigger headaches with closed-source software. Vendors can completely change the algorithms inside the 'Black box' and the user will not know what has changed and will be unable to discover (e.g. by access to the source code) it either.
  - changes in databases and other online resources lead to changes in results. There are other changes that are beyond a researchers influence. Gene Ontologies are updated and can change from the time of the author's research based upon other publications that curators have used (reflecting the best knowledge currently available). Genome data changes as e.g. Human Genome concensuses that are updated and annotations (both manually curated and compuationally generated) change accordingly.
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

### References ###
Domesday Redux: The rescue of the BBC Domesday Project videodiscs, Jeffrey Darlington, Andy Finney and Adrian Pearce
Publication Date: 30-July-2003, Publication: Ariadne Issue 36
Originating URL: http://www.ariadne.ac.uk/issue36/tna/
