# Artifact for "Alphuzz: Monte Carlo Search on Seed-Mutation Tree for Coverage-Guided Fuzzing"

This repository provides the guidance and all the information needed to reproduce the experimental results reported in the paper.

This *README.md* file describes the structure of the artifact and gives basic information on the content of this artifact.

The 'Artifact_for_Alphuzz.pdf' file gives detail information on how to repreduce the experimental results reported in the paper.


## Artifact content

## "src" directory

We implement two prototypes of our seed scheduling strategy. They are Alphuzz on top of AFL, and Alphuzz++ on top of AFL++.

1. Alphuzz - <https://github.com/zzyyrr/Alphuzz.git>
2. Alphuzz++ - <https://github.com/zzyyrr/Alphuzzplusplus.git>


## "docker_image" directory
we provide a Docker image with our prototypes and all the software package dependencies installed.

1. `docker.pdf` describes the usage of the docker image.


## "datasets" directory

We leverage three datasets in our paper. Here, the links to each dataset are provided. In order to facilitate the reproduction, the docker image mentioned above contains all the datasets, initial seeds and scripts used to run the experiments.


1. The CGC dataset. - <https://github.com/trailofbits/cb-multios>
   The initial seeds are provided by the CGC dataset.

2. The UniFuzz dataset. <https://github.com/unifuzz/overview>
   The initial seeds are provided by the UniFuzz dataset.

3. 12 real-world binaries. 
   The `real_world_programs.xlsx` file gives the information on the 12 real-world binaries.
   The initial seeds come from the default seed examples provided by AFL.


