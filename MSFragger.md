A very-well known algorithm that searches spectra against peptide databases, comparing experimental to theoretical spectra and using a similarity metric to make a call on the fragment. Known for using a fragment index which significantly reduces resource use, making searching feasible on an above average desktop
**Note**: ***this explanation is sourced from Sage (https://lazear.github.io/sage/) and thus the implementation is slightly different***

## How it works:
- perform in-silico digest of proteome database 
	- this is our reference, but proteins are digested in MS analysis. Trypsin is an enzyme used for this, creating a predictable cleaving pattern and the resulting peptides fragment in a predictable manner
- get rid of duplicates
- sort digested peptides by mass
- generate and collect all b- and y- fragment ions for every peptide
- sort list by fragment mass / z
- put into bins of 16 fragment size
- sort bin by precursor mass
- give each bin a key that is the minimum fragment mass
- Use [[B+ Tree]] to search