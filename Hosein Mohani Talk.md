11/10/2023
- Mining metagenomic datasets for low abundance/uncultivatable molecules
- BGC - biosynthetic gene clusters
- for identifying molecules: microbial genomes -> BGCs -> molecules
- Pipeline: sample - > SPades (metagenome alignment) -> antiSMASH (predicting BGCs) -> protein graph representation -> graph digestion (??) -> theoretical mass spec
	- in parallel: sample -> MS
- **MolDiscover**: ML MS fragmentation of small molecules
	- small molecule -> calc all possible fragmentations -> annotate theoretical spectra of fragments -> train against MS dataset, to find the occurence bond type breakage -> likeliness of experimental MS to be molecules based on this logrank bond breakage prob. table
- **Efficient spectral library search and clustering**:
	- Like MSFragger: store spectra by peak mass, can be accessed by peak mass
	- reduces time in molecular networking (sounds like clustering molecules)


Use MCMC to estimate statistical significance of peptides and use decoy-target method