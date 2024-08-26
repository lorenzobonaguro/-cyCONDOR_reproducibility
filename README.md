# *cyCONDOR* - an integrated ecosystem for high-dimensional cytometry analysis
</br>

## Abstract
High-dimensional cytometry (HDC) is a powerful technology for studying single-cell phenotypes in complex biological systems. Although technological developments and affordability have made HDC broadly available in recent years, technological advances were not coupled with an adequate development of analytical methods that can take full advantage of the complex data generated. While several analytical platforms and bioinformatics tools have become available for the analysis of HDC data, they are either web-hosted with limited scalability or designed for expert computational biologists, making their use unapproachable for wet lab scientists. Additionally, end-to-end HDC data analysis is further hampered as unified analytical ecosystems are missing, requiring researchers to navigate multiple platforms and software packages to complete the analysis.
To bridge this data analysis gap in HDC we developed cyCONDOR, an easy-to-use computational framework covering not only all essential steps of cytometry data analysis but also including an array of downstream functions and tools to expand the biological interpretation of the data. The comprehensive suite of features of cyCONDOR, including guided pre-processing, clustering, dimensionality reduction, and machine learning algorithms, facilitates the seamless integration of cyCONDOR into clinically relevant settings, where scalability and disease classification are paramount for the widespread adoption of HDC in clinical practice. Additionally, the advanced analytical features of cyCONDOR, such as pseudotime analysis and batch integration, provide researchers with the tools to extract deeper insights from their data. We used cyCONDOR on a variety of data from different tissues and technologies demonstrating its versatility to assist the analysis of high dimensionality data from preprocessing to biological interpretation.


## Why this repository?
This repository provides the original code used to prepare each panel of the manuscript, to ensure the reproducibility of the analysis we provide a docker image for an Rstudio session including all required dependencies and the *cyCONDOR* package (v. 0.2.0).

## How to use this repository
We try to provide access to the analysis in the easiest possible way, the user can follow this few instructions and should be able to be up and running quickly. Within each folder you can find all the scripts and data required to reproduce the analysis.  

### Requirements
Some of the calculations, can be quite memory demanding, we suggest a minimum of 32 Gb of system memory.
- [Git](https://git-scm.com/)
- [Docker](https://www.docker.com/)

### Cloning the repository
```sh
# Make a local copy of the repository
git clone https://github.com/lorenzobonaguro/cyCONDOR_reproducibility

# Navigate to the folder
cd cyCONDOR_reproducibility
```
### Download the Docker image and start the container
```
docker pull lorenzobonaguro/cycondor:v020
```

```sh
# Run a container
docker run -dp 8787:8787 -e USER=mariorossi -e PASSWORD=mariorossi --name rep_condor -v 'your_directory':/home/mariorossi/data/ lorenzobonaguro/cycondor:v020
```

### Open the RStudio session
Enter in your browser `localhost:8787`, this should start a Rstudio session you can use to explore the code and reproduce the analysis.

## How to cite *condor*
If you use *cyCONDOR* in your research project consider citing us [linktojournal](link).

## Contact or follow us
For any problem or question regarding the *condor* package or this repository or you just want to be up to date on what is coming next, send us an [email](mailto:lorenzobonaguro@uni-bonn.de) or follow us:  [@LorenzoBonaguro](https://twitter.com/LorenzoBonaguro)
