# Lecture (10/30/2023)

# [[Epigenetics]]
### [[Chromatin Organization]]
- **Nucleosomes**: first level of compaction of the human genome
	- complex of eight **histones**
	- Nucleosomes compact DNA 5-10x 
	- diploid human cell with 2 copies of genome and ~6 bill bp has approx 30 mill nucleosomes
- **Histone H1**: second level of compaction
	- compacts genome by interacting with nucleosomes, compacting them into sort of a spiral shape
- **third level**: 30nm fibers organized into 300nm by scaffolding proteins
- **fourth**: 700nm fibers
- **fifth**: final compacted into chromosome state
- **DNA accessibility**: shape plays a role in regulation
	- **Euchromatin**: open and considered active
	- **Heterochromatin**: condensed and inactive
	- Histone and/or DNA modifications dynamically change accessibility
### [[DNA Methylation]]
- **Methylation**: deactivates gene expression
	- occurs on cytosines in the DNA
	- Methylated by methylating enzymes
- Methylated DNA is binding site for chromatin remodeling proteins, which condenses chromatin
- Also inhibits TF binding
### [[Histones]]
- Form octamers with each other, nucleosome
- rich in Lysine and Arginine amino acids: positively charged at neutral pH
- N-terminus of each histone protein sticks out from nucleosome and looks like a tail
	- subject to different modifications that affect DNA accessibility
- **Common Modifications**: Methylation and Acetylation
	- H3 and H4 are usual targets of these mods
	- >50 sites are known to be modified on histone tails
- **Acetylation**: adding acetyl group to Lysine (K)
	- masks positive charge of Lysine amino acid
	- weakens interaction between histone and negatively charged DNA
	- opens up genome, "turns on" genome
- **Methylation (histones)**: Lysines (K) and Arginines
	- can either activate or repress genes, depending on the amino acid on which amino acid is being methylated
	- **Mono, Di, or Tri** methylation:
		- *H3K4me1, H3K4me2, H3K4me3*: Histone H3's Lysine at residue 4 is methylated one, two, three times

- **Electrophoretic Mobility Shift Assays**: EMSA, combine labeled piece of DNA with a protein
	- run a gel on samples of binding DNA and protein
	- protein adds weight to protein: slows down DNA radiation bend in gel analysis

## [[ChIP-Seq]]
- Chromatin Immunoprecipitation next generation sequencing
- can determine location in genome of a particular histone with a specific methylation
- determine where a specific protein is interacting with DNA
- **Protocol**:
	- Add cross-linking agent (formaldehyde) to fix DNA/protein interactions
	- Lyse cells
	- Fragment DNA into uniform size pieces
	- Add magnetic bead conjugated antibodies
	- Use magnets to isolate Antibody-Protein-DNA complexes
	- Use heat to reverse crosslinks, release DNA
	- Isolate and sequence DNA
	- Use peak finding software to identify regions

#### Example of ChipSEQ: NRSF/REST Transcriptional Repressor
- silencing TF
- negative regulator
- inhibits by recruiting histone deacetylases to genome promoters
- Histone Deacetylation promotes closed form of chromatin
- Really well characterized binding protein: ~80 known binding sites in human genome
	- also has high-quality antibody
- Found 1946 enriched regions
	- subset of regions contain 1 or 2 canonical binding sites
	- without known binding sites: hmmm
	- canonical binding sites line up veryyyy well
	- found peaks at computationally predicted binding sites
	- top 10% canonical peaks were plugged into MEME algorithm to get a SINGLE motif: separation of 2nt
	- same happened for noncanonical, except separated by 11nt
- shown novel binding site of first exon in NeuroD1 gene

### ENCODE
- encyclopedia of DNA elements
- multi-national consortium follow up to human genome project
- **Discoveries**:
	- histone modification patterns are highly predictive of gene TSSs
		- also where TFs bind to genome


# Lecture 11/1/2023
# [[DNA Sequencing]]
## [[Sanger Sequencing]]
- **dideoxyribonuclease triphosphate (ddNTPs)**: does not have a hydroxyl group at 3' carbon, so strand can not be extended on the 3' end
- prepare primer with DNA of interest
- include small amounts of ddNTPs in mixture
	- this stops strand extension when ddNTP is added
- in separate ddNTP and DNA polymerase mixtures, find lengths of separate DNA strands
	- N length strand in ddNTP mix, base is at Nth position
	- determined by gel electrophoresis
- Note: SNPs can mess up gels, make two nucleotides look like they're from the same position
- Labeling:
	- label primer
	- label dNTP
	- label ddNTP
- Currently: instead of gels
	- laser detection of different bases suspended in a capillary gel
- **Capillary gel**: gels are in thin capillaries with charge difference at ends
- to determine whether mutation in intensity plot: sequence from both sides
- High accuracy, low volume
- can be read in parallel
# Human Genome Project
- **[[Shotgun Sequencing]]**: assemble contigs from PCR amplified regions
	- proposed in middle of project to speed up sequencing
	- trouble with contig flipping, orientation is unknown
- Moore's law and cost per genome have correlation

# [[Next Generation Sequencing]]
- Massively parallel sequencing
- Attach adapters to DNA molecules
	- terminus on other end binds to terminator in flow cell
	- bend becomes double stranded
	- amplify signals to show clusters
	- sequence by synthesis (SBS): synthesize other strand, get signal by adding one base at a time



