### 11/9/2023
- potentially adding alphapeptdeep and GPU access to fragpipe
- Ryna presentation: 
### Normalization mehotds in mass spec analytical proteomics
- study to find out what normalization methods are most appropriate for different situations
- Z score normalization, median divide normalization, quantile normalization
- 4 different sets of (ccRCC, chRCC, RO, and NAT) renal cell carcinoma tissues
- MaxLFQ on Maxquant used for quantification
- anlaysis and processing done through Perseus
	- for individual proteins quantile normalization consistently had higher number of protein calls when compared to Z-score (slightly) and Median divide (largely)
	- for identifying protein groups: not much of a difference