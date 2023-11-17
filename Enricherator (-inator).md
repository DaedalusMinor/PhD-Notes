- infers enrichment compared to baseline
	- Fits GLM to seq data using variational inference
	- kind of an interpolation, to account for gaps in enrichment. gaps dont follow natural laws
	- weight matrix responsible for local pooling of sparse fitted input DNA
	- prior dist of N(0,4) - hardcoded variance, just assumed
- Also ShapeME: sequence and shape inference
	- shape vs. sequence motifs
		- shape predicts dna-protein interactions better
		- shape most likely contains information that seq info provides
		- much larger edit distance between sequences when compared to manhattan distance differences between shapes
	- identifying motifs using mutual info:
		- looking at mutual identification of peak and motif
		- calc mutual info for each seed
	- tweak shape weights to maximize mutual info