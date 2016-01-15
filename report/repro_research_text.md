### Computational Reproducibility: Workshop Report ###
Reproducible Research: A long and winding road.

#### Introduction ####
Reproducibility is often cited as a core tenet of the Scientific method; Indeed Einstein is quoted as saying "Insanity: doing the same thing over and over again and expecting different results." But what do we mean by reproducibility? How do we define it? Why and how should we strive for it in our research?
  - motivation for reproducibility (cite Florian?)
  - cost/benefit analysis
  Reproducibility does not come for free and , as can be seen later in this paper, can involve considerable effort and a broad skill-base to achieve it. It is therefore reasonable to question - is it worth it?
There is some evidence supporting the concept that papers whose research is reproducible are more highly cited than those which are not.
Reproducibility can also assist in techniques and tools to be repurposed to address new scientific questions which is another desirable research outcome.
Greater stability in our confidence in conclusions drawn from bioinformatic analyses can come from greater robustness of preceding works given how this area of science is so heavily interdependant on derivations from previously annotated data and inferences.
  - The target audience of this paper include the folloowing stakeholders: computational scientists, wet biologists and research funders. They have differing roles and rsponsibilities on the road to reproducible research but all are key to the endeavour.

#### Levels of Reproducibility ####

  - **computational auditability**
  By computational auditablity we mean - is it possible to follow the tools and techniques used to analyse the data and derive broadly similar (if not identical) results and conclusions? This requires a certain measre of discipline in recording the 'big picture' of the study capturing not just the exact tools, techniques and data but the entire narrative i.e. the assumptions, decisions and reasoning  used in the analysis. Later we will explore tools that assist researchers in achieving this goal.
    - cannot reasonably reproduce, say, ENCODE
    - can leave a sufficiently clear audit/log trail
    - allows for scrutiny of 
  - **mechanical reproducibility**
    - reproduce figures/tables/numbers from raw data
    - does not imply correctness, but at least can see what was done
    - what duration are we targeting? 5 years? 10 years? 20? 50?  Will your Docker image still be runnable in 50 years?
  - **scientific reproducibility**
    - arrive at same conclusions via different analysis paths
    - clearly a problem if your result depends on, say, a particular version of some software package
    - not clear what counts as "same conclusions": how much wiggle room is okay?

#### Problem Areas ####

  - versions of software. Programs by their very nature evolve and develop with new features and different libraries being developed and used. Whilst this is great as far as developing new features and capabilities, it comes at the cost of potentially wrecking backwards compatibility with previous versions and delivering different results.
  - Computational efficiency - Many released tools have large memory footprints (e.g. Assemblers) requiring high-spec computers or clusters as the computational bar to reproducing the analysis. This precludes a large segment of people as they either do not possess/have access to/can afford such resources. It is possible to develop software with low memory footprints as a design goal. An example of this is the GATB: Genome Assembly & Analysis Tool Box.
  - It is extremely important for software authors/package maintainers to be scrupulous in documenting changes occurring in new releases of packages, especially if it may break reproducibility. The good programming practice of unit testing e.g. pytest in Python should be encouraged during software development. Another driver for good documentation is the acceptance that people move on from projects (and sometimes completely leave science) and may no longer be willing or able to offer support for a tool or package.
http://phdcomics.com/comics.php?f=1689
  - closed-source packages. Versioning can cause ven bigger headaches with closed-source software. Vendors can completely change the algorithms inside the 'Black box' and the user will not know what has changed and will be unable to discover (e.g. by access to the source code) it either. This approach often also proliferates proprietary data formats which also hinder reproducibility and usage at a later date (See paper on the Domesday Project).
  - changes in databases and other online resources lead to changes in results. There are other changes that are beyond a researchers influence. Gene Ontologies are updated and can change from the time of the author's research based upon other publications that curators have used (reflecting the best knowledge currently available). Genome data changes as e.g. Human Genome concensuses that are updated and annotations (both manually curated and compuationally derived) change accordingly.
  - assumptions underlying analysis
  - fragile analyses
  - cost of reproducibility, lack of benefits
Clearly reproducibility can take considerable effort and the benefits are not manifestly clear.

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
E. Drezen, G. Rizk, R. Chikhi, C. Deltel, C. Lemaitre, P. Peterlongo, D. Lavenier, GATB: Genome Assembly & Analysis Tool Box, Bioinformatics, 2014 http://bioinformatics.oxfordjournals.org/content/early/2014/06/30/bioinformatics.btu406.abstract?keytype=ref&ijkey=koXTzqbf4Nt1kVO
Sandve GK, Nekrutenko A, Taylor J, Hovig E (2013) Ten Simple Rules for Reproducible Computational Research. PLoS Comput Biol 9(10): e1003285. doi:10.1371/journal.pcbi.1003285

