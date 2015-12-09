## Reproducible Research I Summary ##

#### The Long and winding road to Reproducible Research ####

### Introduction ###
The desire that research be reproducible is not new. Research papers document a piece of research outlining the questions  asked,  protocols used, analysis used, decisions made and conclusions reached – or do they? There is a growing interest in achieving reproducible research, especially in computational research.
A valid question is why should we be concerned about reproducible research? If it requires even more effort to ensure it, is the game worth the candle?

Bioinformatics is an area of science that relies heavily upon what has gone before and on building upon it. So it is extremely reliant upon there being no flaws in the foundations.

A recent workshop meeting held at CR-UK, Cambridge Institute focussed upon the goals, challenges, costs, benefits and achievability of Reproducible Research.

A oft-mentioned exercise entailed asking students to reproduce the analysis outlined in a current research paper. This exercise can serve to highlight the ways in which authors can (unintentionally) hamper the reproducibility of their research.

### Goals ###

Where the research and its techniques are reproducible, they can be more easily and efficiently applied to new areas making the work more valuable and citeable. If methods and analysis are incomplete then this can be frustrating for other researchers.

The goal of public trust in scientists and their research is greatly assisted by transparency and openness as is the important task of peer review. Retracted papers can often damage that trust.

Clarity in decisions made by the researcher i.e. why particular filters were used and what assumptions were applied in the analysis. It was felt desirable that research communications captured the ‘bigger picture’ i.e. the reasoning used in experimental design and analysis.

### Challenges ###

Technologies such as Next Generation Sequencing are disruptive technologies and frequently evolve. This results in a proliferation of data formats and content. Even when there is a particular format, they are not set in stone e.g. FASTQ

IT is also not a stable environment -- software tools evolve as do their supporting libraries. Often older versions become unavailable e.g. the number of retained versions in Bioconductor. Changes in accuracy can also come from hardware advances.

Many software tools require a complex supporting ecosystem and it can be a challenge to put all of this in place to run one particular tool. An example of this (and by no means alone) is the QIIME pipeline for microbiome analysis.
Also, there may be tools on the same machine wanting different versions of libraries or languages and these often do not happily coexist. 

Conventional command-line bioinformatics pipelines can be challenging for occasional users and a number of skills are required to make such scripts deployable and reproducible. 

Traditional print journals put restriction on the length of papers due to the physical restraints of the media. This can push material out into 'supplemental material' which may not be peer-reviewed.
Many bioinformatics pipelines rely upon considerable computational resources to be achievable which can set a high overhead to an ability for other scientists aiming to reproduce the analysis even when the tools and original data have been published and are freely available. 

All of this conspires to confound efforts to provide an accessible stable environment to support reproducible analyses.
Fortunately, disruptive technology can also provide some of the answers as well as providing the If RR is to be achieved it should be problems.

Sweave, Knitr, Pandoc, LaTEX, Rmarkdown (Example of Martijn Wieling presentations).

Virtual Machines (like VirtualBox) offer many advantages. Researchers can run an emulated ready-made linux machine on their Windows or Mac computer without losing their existing operating system. A couple of examples where this is used to good effect are the QIIME & Bio-Linux virtual appliances. Extending the functionality of these appliances does need Linux skills which if possessed might be better employed in configuring a native installation. Virtual machines also have a performance overhead due to the emulation that may not be appreciated in compute-intensive tasks.

Docker & Docker Toolbox

Galaxy

Packrat creates a private package library with your scripts so as to maintain package availability over time.

Cloud computing -- can make it easier for people to repeat analysis without needing to have access e.g. to local High Performance Computing resources. Tools like StarCluster facilitate creation of clusters using Amazon Web Services spot instance pricing to provide computation power at lower cost.

Additional reproducibility can be achieved by deploying in Docker containers (Widely supported by Cloud Computing providers (Amazon, Google, Digital Ocean, IBM etc) and/or as cloud instances.

Open Access journals -- mostly published on-line without space restrictions e.g. Nature recently relaxed limits on Materials and Methods section.

### Costs ###

Reproducibility requires consideration from the outset and should be integrated into every stage of the research project from grant submission to the paper(s).

Often the reproducibility work falls upon the analyst in the paper who will not generally be a lead author. This means more effort without the career performance indicator. A putative solution is for there to be an analysis paper and maybe to consider a new role as an adjunct to lead author: Lead Analyst.

Training researchers in computational skills can involve a number of courses including, but not limited to, command-line Linux, basic programming & scripting, version control (e.g. Git), statistics (Experimental design & Analysis)

### Benefits ###

There is some evidence that reproducible papers benefit from higher citation. 
Reduction of risk of retracted papers.
Reinforced Quality Assurance.
Enhanced reusability of techniques in addressing new biological questions.

### Conclusions/summary ###

Buy-in from all parties from grant-funding bodies, research organisations through to journals will reinforce reproducibility as best practice.

Incorporation of Reproducibility into Research Quality Assurance

Make available infrastructure to implement RR

Make training available to empower researches to achieve RR

### References ###

Sandve GK, Nekrutenko A, Taylor J, Hovig E (2013) Ten Simple Rules for Reproducible Computational Research. PLoS Comput Biol 9(10): e1003285. doi:10.1371/journal.pcbi.1003285

### Resources ###

* FASTQ variants  https://en.wikipedia.org/wiki/FASTQ_format 
* Sweave https://www.statistik.lmu.de/~leisch/Sweave/ 
* Friedrich Leisch. Sweave: Dynamic generation of statistical reports using literate data analysis. In Wolfgang Härdle and Bernd Rönz, editors, Compstat 2002 - Proceedings in Computational Statistics, pages 575-580. Physica Verlag, Heidelberg, 2002. ISBN 3-7908-1517-9. [ bib | PDF ]
* Knitr http://yihui.name/knitr/ 
* LaTEX https://www.latex-project.org/ 
* Rmarkdown http://rmarkdown.rstudio.com/ 
* Jupyter http://jupyter.org/ 
* Docker https://www.docker.com/ 
* Docker Toolbox https://www.docker.com/docker-toolbox 
* Shiny  http://shiny.rstudio.com/ 
* Galaxy https://galaxyproject.org/ 
* Rcommander http://www.rcommander.com/ 
* Bioconductor https://www.bioconductor.org/ 
* QIIME http://qiime.org/ 
* Packrat https://rstudio.github.io/packrat/ 
* VirtualBox https://www.virtualbox.org/ 
* Bio-Linux http://environmentalomics.org/bio-linux/ 
* Git & GitHub https://git-scm.com/ & https://github.com/ 
* Starcluster http://star.mit.edu/cluster/ 
* Reproducibility Workshop presentations http://bioinformatics-core-shared-training.github.io/reproducibility_workshop/ 
* Martijn Wieling presentations http://www.martijnwieling.npresentations 
