# DMPfold

## NB this repo is under development and is not ready for production use

Fast de novo protein model generation from covarying sequences using predicted distances and iterative model building.
See the [pre-print](https://arxiv.org/abs/1811.12355) for more.

## Requirements

You will need to have the following software installed:

- HH-suite with database
- CCMPred
- CNS

This repo also includes other software in binary form:

- PSIPRED
- PSICOV
- FreeContact

## Installation

...

## Usage

Example of running on CASP12 target T0864:

- `csh seq2maps.csh T0864.fasta` to run hhblits, PSIBLAST, PSIPRED, SOLVPRED, PSICOV, EVfold, CCMpred, alnstats and output 21c, map and fix files.
- `sh run_dmpfold.sh T0864.fasta T0864.21c T0864.map ./T0864` where the last parameter is an output directory that will be created

Running `sh run_dmpfold.sh T0864.fasta T0864.21c T0864.map ./T0864 5 20` instead runs 5 iterations with 20 models per iteration (default is 3 and 50).
