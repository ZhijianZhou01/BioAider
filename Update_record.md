# Bioinformatics Aider (BioAider)

## Releases: https://github.com/ZhijianZhou01/BioAider/releases

## Latest version: BioAider V1.527 (Feb 21, 2023)


# Revision history


## BioAider V1.0 (May 27, 2020)
+ The first version of BioAider V1.x.


## BioAider V1.03 (Jul 22, 2020)
+ Rewrite and beautify the interface of program, add more prompts for controls.
+ Add a Linux dsitribution (GUI) for Ubuntu (16.04 and more) users.
+ Added multiple sets of codon table in multiple-sequence alignment and in features of “Mutation analysis”.
+ Add variation analysis of non-coding gene and amino acid sequence in features of “Mutation analysis”.
+ Increased the pop-up window of program bug and toolbar for some common features.
+ Add some new other features and fixed some bugs.
+ Provide graphical interfaces for three popular multiple-sequence alignment tools ([MAFFT](https://academic.oup.com/mbe/article/30/4/772/1073398), [Muscle](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-5-113), [Clustal-Omega](https://www.embopress.org/doi/full/10.1038/msb.2011.75)), to facilitate parameter setting and usage. What's more, provide translation-alignment for codon gene. The copy of these tools is in https://github.com/ZhijianZhou01/plugins. Thanks to the developers of these programs. If you need them, please unzip external_program.zip and put the directory external_program in the root directory of the BioAider.


## BioAider V1.314 (Sep 2, 2020)
+ Add the feature of looking for repetitive fragments.
+ Add the feature of locating the protein to the nucleotide sequence.


## BioAider V1.334 (Mar 28, 2021)
+ Add the following functions:
    + Viral *.gb file parser: Extract the information from virus *.gb file, such as host, collection date and country, reference article, etc. What's more, BioAider can be extracted and stored according to species relationship.
    + Ambiguous Base Edition: Processing ambiguous bases and premature stop codons (preparing sequences for PAML analysis).
    + Delete Low-Similar Sequence: Removing sequences with similarity below the threshold.
    + Date converted to Decimal: Convert date to decimal.
    + Sequence Batch Download (NCBI): NCBI sequence batch search.
    + File Merge: Simple function of combining multiple files into one file.
    + Increased the output linked mutation sites and re-beautified the mapping in Mutation analysis function.
    + Provide graphical interface for [FastTree](https://www.embopress.org/doi/full/10.1038/msb.2011.75) software, to facilitate parameter setting and usage. Thanks to the FastTree development team. The copy of FastTree software is in https://github.com/ZhijianZhou01/plugins. If you need it, please unzip external_program.zip and put the directory external_program in the root directory of the BioAider.

+ Fix bugs
    + Mutation Analysis function: Fixed the bug that the "number of stop codons" cannot be counted in the summary file.

+ Please pay special attention:
On April 24, 2021 (International Veterinary Day), we uploaded the BioAider distribution for MacOS system for the first time, and fixed some bugs in the last uploaded windows and linux version (but keep the version number 1.334 unchanged).


## BioAider V1.423 (Mar 24, 2022)
### Fix bugs
+ <b>(Important)</b> the output result of "Codon method" in mutations analysis.
  + Resolved the bug that could not correctly plot the frequency distribution of synonymous and non-synonymous substitution sites using "base" as the statistical unit (the result of "_substitution frequency distribution.pdf" and "_single syn or non-syn substitution nt sites.csv" and "*_Frequency group of sys and non-sys substitution.txt") when there are a large number of different kinds of mutations at the same codon site (e.g. sequences are from different genera or species, or large number of dinucleotide and trinucleotide substitution sites). Note that even if this bug is resolved, it is not recommended to apply it to the sequence sets with a large variety of variants at the same codon site, because it maybe no real value to count the number of nucleotides sites based on mutation frequency.
    <b>Tip: </b>Statistical results (such as *_all site.csv and *_mutation site.csv) using "codons" as units are correct for any sequences in the previous version.

  + Resolved the bug that incorrect count of nt in "Others information" part in the end of "_mutation site summary.txt" when there are a large number of dinucleotide and trinucleotide substitution sites in sequence sets.
    <b>Tip: </b>Except for the "Others information" part, everything else in "_mutation site summary.txt" is correct in the previous version.

+ Solved the problem that "Delete Lower similar sequences" cannot run in BioAider v1.334.

+ The problem that the input file or directory cannot contain "."

### Add new functions
+ <b>(New and important)</b> Optimized algorithm to greatly speed up BioAider, and quickly perform mutation analysis on hundreds of thousands of pieces of data (2022/03/24).

+ "Codon" method of mutation analysis add the option to delete "nt sites with both synonymous and nonsynonymous substitution" freely when drawing the graph of "frequency distribution of synonymous and non-synonymous substitution sites".

+ (New and important) Function for drawing a lollipop map of gene (or genome) mutation sites.
+ Function to draw scatter,boxplots, violin diagram for data based on seaborn package (GUI interface).
+ Function to switch various themes freely.


## BioAider V1.527 (Feb 21, 2023)
### Add new functions

+ Provides tools for hierarchical clustering based on k-mer features of nucleotide sequence.

+ Added options for nucleotide, codon and amino acid in the Linked mode of <b>"Mutation Analysis"</b>. 

+ For codon data, add the output result in <b>"Mutation Analysis"</b> that can be used to draw mutant lollipops.

+ Support multiple opening of the same pop-up window to run multiple data at the same time.

+ Provides an <b>efficient electronic-lab-notebook</b> to support recording experiments and managing them.
  
+ Increase update detection of software version, including manual and automatic one.

+ Support changing font and font size of software.

+ Add codon-extraction function in <b>"Sequence Vary"</b>, including two modes, (1, 2 , 3) and (1 + 2, 3).

+ Support adding and deleting shortcuts, quickly access other software while using BioAider.

+ Provide graphical interfaces for some classic command-line  programs
  + Provide the graphical interfaces for [IQ-Tree](https://academic.oup.com/mbe/article/37/5/1530/5721363), [MrBayes](https://doi.org/10.1093/sysbio/sys029) and [ModelFinder](https://www.nature.com/articles/nmeth.4285) softwares, to facilitate parameter setting and usage. These tools are loaded as plugins at the user's choice in BioAider. Thanks to development teams of these classic softwares.
  + Added conversion tool of model parameter, and easily prepare model-files for IQ-Tree and MrBayes When the sequence data is partitioned.
  
  + Provide a graphical interface for [Blast](https://pubmed.ncbi.nlm.nih.gov/2231712/), to facilitate parameter setting and usage. The Blast program is loaded as plugin at the user's choice in BioAider. Greatly simplify library construction and sequence alignment, and provide convenient management of multiple databases. Thanks to development team of Blast software.



### Fix bugs in version 1.423

+ The function of "Repeat Fragment Search" cannot work in BioAider V1.423.
+ The "Remove High-Similar sequences" cannot work in BioAider V1.423.
+ The file directory of the main interface cannot be automatically updated in BioAider V1.423.
+ Some bugs on sorftware interface. Optimize interactive operation and beautify the interface.

