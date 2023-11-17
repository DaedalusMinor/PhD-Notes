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
- Illumina
# Lecture 11/6/2023
## continuing on NGS
- bar codes added to adapters to uniquely identify each sample sequence
# Third Generation Sequencing
- PacBio: long fragments of length 500-8000 after creating a circle with adaptors
	- no PCR
	- sequences molecules in real time
- PacBio II
	- Quicker: 30 minutes to 3 hours
	- longer fragments
	- How it works
		- generate amplicon
		- ligate adaptors: dumbell structure, closes what would be adaptors
		- if denatured, primers form a circle
		- polymerase attached to bottom of small well
		- light signals read as polymerase works on molecule
		- not massively parallel
		- high error rate
		- 20kb reads
		- can distinguish methylated vs. nonmethylated by sequencing delay
		- Another method allows circular DNA to be sequenced mutliple times in a single well by repeated
- Ion Torrent:
	- highly uniform coverage
	- wave difference of hydrogen proton release that happens during synthesis
	- eliminate sequence error sources: 
		- modified bases
		- fluorescence
	- much faster
- Oxford Nanopore: not sequenced by synthesis
	- helicase-pore complex brings double strand to complex, unzips as single strand goes through pore
	- ion current being passed through pore, bases interrupt current in unique way
	- 4 million reads, and can also use short read sequencing that is 50 to 300 bp long
- combination:
	- PacBio and short read assembly helps improved assembly quality
- Sequence capture:
	- before sequencing, hybridize and elute DNA you want to capture
	- most popular: exome sequencing capture all human exomes and surrounding DNA regions
		- some exomes are better sequenced than others
	- custom capture: using "panels"
		- only look at genes of interest e.g. cancer causing genes

### Applications of NGS/3GS
- **RNA sequencing**: digital gene expression ??
- **ChIP-Seq**: 
- De Novo Sequencing: without reference
- resequencing after capture

# Lecture 11/8/2023
## Variants in Human DNA
- 14 Million SNPs, or around 1 mill common human snps
- most common form of variant
- 12% of human genome is affected by CNVs (copy number variations)
- CNVs:
	- change in the number or copies of loci
	- ***de novo***: CNV that is not inherited
	- Microdeletions 
	- **Recurrent**: associated with distinct but variable phenotypes. formed by NAHR during meiosis mediated by flanking repeat sequences and are associated with hotspots for rearrangement
	- **non-recurrent**: arise across genome and appear to be formed by unclear homologous repair mechanisms
- de novo mutations in autism and schizo
	- 6-7% autism cases are known to have cytogenetic abnormality
	- 10% of cases of autism de novo CNVs found
	- de novo CNVs have been found increased in SZ
	- CNV locus 1q21.1 deletion can increase chances of ID and SCZ by factor of about 10, statistically insignificant change for ASD
- CNVs in health
	- accounts for 10-15% for severe intellectual disabilities or neuro disorders
	- Normal CNV mutation rate estimated to be 0.01-0.03 mutations per haploid genome per generation

## Genome wide SNPs studies
- Linkage disequilibrium
- for finding SNPs use Illumina chips: using beads with primers and ddNTPs that antibodies bind to and create signals for specific bases
- only capture signal for two bases
	- most SNPs are C/A or C/T alleles
	- SNP chip:
		- 300k - 500k common tag snps
		- 6k - 10k common snps for linkage
		- 300k exome missense or LOF coding SNPs 
		- 50k SNPs that are added for custom content
	- Most original SNP arrays are biased for Caucasians
- Can use PCR to show a deletion
- Chromosomal microarrays (CMA)
- competitive genomic hybridization (CGH)
- region of homozygosity, way to see if you have a deletion

### What is genetic testing used for?
- comfort in knowing where disease comes from
- recurrence risk within the family


# Lecture 11/13/2023
## [[Genome Wide Association (GWA)]]
- Genetic association test
- Most SNPs differ in allele frequency by population, even by subpopulaiton
	- to examine stratification, use PCA to separate populations
	- idea behind ancestry searches
- QQ plots: Quality control 
	- expected vs. observed
- manhattan plots:
	- examining clusters of SNPs
	- a lot of SNPs in human genome are highly correlated
	- one snp that causes association
- confounding association by ethnicity
- effect sizes of GWAS SNPs are typically small
- genes found by GWAS increase with sample size
- the more samples the more SNPs
	- with 100,000 samples, usually identify 10-100 SNPs
	- usually explain about 1-3% of variance, and 2-5% of genetic variance (~50 inheritable)
- Polygenic genetic risk scores (PRS or PGRS)
	- Multinomial logistic regression procedure with model selection to identify the best fitting model of relations between phenotype and genotype (PRSice)
		- used to show relationship between psychiatric disorders
***Genetics contributes to severe respiratory COVID19***
- *The phenotype was respiratory failure*: the use of oxygen supplementation or mechanical ventilation
	- severity was graded 
	- split between mechanical and non mechanical ventilation

# Lecture 11/15/2023
## [[Cell differentiation]]
- two ways of making sister cells different
	- *asymmetric*: difference in factors arranged in mother cell
	- *symmetric*: difference in environmental factors after sister cells have been created
- *inductive signal*: cells signal to neighboring cells, either to dissuade or encourage differentiation into their cell type
- Three main embryonic layers:
	- endoderm: lung cells, digestive tract, thyroid cells
	- mesoderm: cardiac muscle cells, red blood cells, smooth muscle cells
	- ectoderm: skin and neuron
- formation of epithelial tube: epithelial cells separte the inside from the outside of the body
	- invagination, specific regions of sheet become pinched off into an epithelial tube
- drosophila: localized mRNAs direct localized differentiation in Drosophila
	- morphogen gradients -> strict areas of gene transcription -> strict differentiated areas of protein translation
	- Homeotic genes are conserved: Hox genes are conserved across drosophila, mice, and humans
## [[Stem Cells]]
- cant go back to stem cell after differentiation
- gradient of differentiation in cells, stem cells going up become more specialized in skin and gut lining 
- what is a stem cell:
	- 1. stem cells are not terminally differentiated
	- 2. stem cells can divide without limit
	- 3. during cell division, daughter cells can: stay a stem cell or commit to terminal differentiation path
- characterized by presence of transcription factor markers
- different types
	- *Adult*: limited range of cell types, tissue-specific
		- rare
		- found in bone marrow
	- *embryonic*: found in early embryos, differentiate into any cell type
		- advantage over adult
			- wide range of differentiation
			- easier to grow
			- UM has greatest academic collection of ES cells from people with genetic disorders
- transfection of mouse cells and human cells with certain transcription factors could reprogram them into iPS
	- iPS cells can be induced into many cell types
- stem cell therapeutics:
	- proliferate extensively to generate sufficient quantities while maintaining potential to differentiate into the desired cell type(s)
	- survive in recipient after transplant
	- integrate into tissue
	- function long term
	- avoid harming recipient (growing into cancer cells)

## Cancer
- genetic changes: 
	- deletion/mutation of tumor suppressor genes
	- activation of oncogenes