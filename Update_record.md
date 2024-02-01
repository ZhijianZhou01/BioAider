# Bioinformatics Aider (BioAider)

## Releases: https://github.com/ZhijianZhou01/BioAider/releases

## Latest version: BioAider V1.527 (Feb 21, 2023)


# Revision history


## BioAider V1.0 (May 27, 2020)
+ The first version of BioAider V1.x.


## BioAider V1.03 (Jul 22, 2020)
+ Rewrite and beautify the interface of program, add more prompts for controls.
+ Add a Linux dsitribution (GUI) for Ubuntu (16.04 and more) users.
+ Added multiple sets of codon table in multiple-sequence alignment and in features of <b>```Mutation Analysis```</b>.
+ Add variation analysis of non-coding gene and amino acid sequence in features of <b>```Mutation Analysis```</b>.
+ Increased the pop-up window of program bug and toolbar for some common features.
+ Add some new other features and fixed some bugs.
+ Provide graphical interfaces for three popular multiple-sequence alignment tools ([MAFFT](https://academic.oup.com/mbe/article/30/4/772/1073398), [Muscle](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-5-113), [Clustal-Omega](https://www.embopress.org/doi/full/10.1038/msb.2011.75)), to facilitate parameter setting and usage. What's more, provide translation-alignment for codon gene. The copy of these tools is in https://github.com/ZhijianZhou01/plugins. Thanks to the developers of these programs. If you need them, please unzip ```external_program.zip``` and put the directory ```external_program``` in the root directory of the BioAider.


## BioAider V1.314 (Sep 2, 2020)
+ Add the feature of ```looking for repetitive fragments```.
+ Add the feature of ```locating the protein to the nucleotide sequence```.


## BioAider V1.334 (Mar 28, 2021)
+ Add the following functions:
    + <b>```Viral *.gb file parser```</b>: Extract the information from virus *.gb file, such as host, collection date and country, reference article, etc. What's more, BioAider can be extracted and stored according to species relationship.
    + <b>```Ambiguous Base Edition```</b>: Processing ambiguous bases and premature stop codons (preparing sequences for PAML analysis). This feature was contributed by Xiyue Wang. In addition, the authors suggest: (i) the content of ambiguous bases in a single sequence should not be greater than 2%;  (ii) it is not suitable to correct the ambiguity base sites in those sequences with long genetic distances.
    + <b>```Delete Low-Similar Sequence```</b>: Removing sequences with similarity below the threshold.
    + <b>```Date converted to Decimal```</b>: Convert date to decimal.
    + <b>```Sequence Batch Download (NCBI)```</b>: NCBI sequence batch search.
    + <b>```File Merge```</b>: Simple function of combining multiple files into one file.
    + Increased the output linked mutation sites and re-beautified the mapping in <b>```Mutation Analysis```</b> function.
    + Provide graphical interface for [FastTree](https://www.embopress.org/doi/full/10.1038/msb.2011.75) software, to facilitate parameter setting and usage. Thanks to the FastTree development team. The copy of FastTree software is in https://github.com/ZhijianZhou01/plugins. If you need it, please unzip ```external_program.zip``` and put the directory ```external_program``` in the root directory of the BioAider.

+ Fix bugs
    + Fixed the bug that the ``number of stop codons`` sometime cannot be counted in the summary file in <b>```Mutation Analysis```</b>  function.

+ Please pay special attention:
On April 24, 2021 (International Veterinary Day), we uploaded the BioAider distribution for MacOS system for the first time, and fixed some bugs in the last uploaded windows and linux version (but keep the version number 1.334 unchanged).


## BioAider V1.423 (Mar 24, 2022)
### Fix bugs
+ <b>(Important)</b> the output result of <b>"Codon method"</b> in <b>```Mutations Analysis```</b>.
  + Resolved the bug that could not correctly plot the frequency distribution of synonymous and non-synonymous substitution sites using "base" as the statistical unit (the result of ```_substitution frequency distribution.pdf``` and ```_single syn or non-syn substitution nt sites.csv``` and ```*_Frequency group of sys and non-sys substitution.txt```) when there are a large number of different kinds of mutations at the same codon site (e.g. sequences are from different genera or species, or large number of dinucleotide and trinucleotide substitution sites). <b>Note that even if this bug is resolved, it is not recommended to apply it to the sequence sets with a large variety of variants at the same codon site, because it maybe no real value to count the number of nucleotides sites based on mutation frequency.</b>
    <b>Tip: </b>Statistical results (such as ```*_all site.csv``` and ```*_mutation site.csv```) using <b>codons</b> as units are correct for any sequences in the previous versions.

  + Resolved the bug that incorrect count of nt in <b>Others information</b> part in the end of ```_mutation site summary.txt``` when there are a large number of dinucleotide and trinucleotide substitution sites in sequence sets.
    <b>Tip: </b>Except for the <b>Others information</b> part, everything else in ```_mutation site summary.txt``` is correct in the previous versions.

+ Solved the problem that <b>```Delete Lower similar sequences```</b> cannot run in BioAider v1.334.

+ The problem that the input file or directory cannot contain ```.```

### Add new functions
+ <b>(New and important)</b> Optimized algorithm to greatly speed up BioAider, and quickly perform mutation analysis on hundreds of thousands of pieces of data (2022/03/24).

+ ``Codon`` method of <b>```Mutation Analysis```</b> add the option to delete ```nt sites with both synonymous and nonsynonymous substitution``` freely when drawing the graph of ```frequency distribution of synonymous and non-synonymous substitution sites.pdf```.

+ (New and important) Function for drawing a lollipop map of gene (or genome) mutation sites.
+ Function to draw scatter, boxplots, violin diagram for data based on seaborn package (GUI interface).
+ Function to switch various themes freely.



## BioAider V1.527 (Feb 21, 2023)
### Add new functions

+ Provides tools for hierarchical clustering based on k-mer features of nucleotide sequence.

+ Added options for nucleotide, codon and amino acid in the Linked mode of <b>```Mutation Analysis```</b>. 

+ For codon data, add the output result in <b>```Mutation Analysis```</b> that can be used to draw mutant lollipops.

+ Support multiple opening of the same pop-up window to run multiple data at the same time.

+ Provides an <b>efficient electronic-lab-notebook</b> to support recording experiments and managing them.
  
+ Increase update detection of software version, including manual and automatic one.

+ Support changing font and font size of software.

+ Add codon-extraction function in <b>```Sequence Vary```</b>, including two modes, (1, 2 , 3) and (1 + 2, 3).

+ Support adding and deleting shortcuts, quickly access other software while using BioAider.

+ Provide graphical interfaces for some classic command-line  programs
  + Provide the graphical interfaces for [IQ-Tree](https://academic.oup.com/mbe/article/37/5/1530/5721363), [MrBayes](https://doi.org/10.1093/sysbio/sys029) and [ModelFinder](https://www.nature.com/articles/nmeth.4285) softwares, to facilitate parameter setting and usage.  These tools are loaded as plugins at the user's choice in BioAider. Thanks to development teams of these classic softwares.
  + Added conversion tool of model parameter, and easily prepare model-files for IQ-Tree and MrBayes When the sequence data is partitioned.
  
  + Provide a graphical interface for [Blast](https://pubmed.ncbi.nlm.nih.gov/2231712/), to facilitate parameter setting and usage. The Blast program is loaded as plugin at the user's choice in BioAider. Greatly simplify library construction and sequence alignment, and provide convenient management of multiple databases. Thanks to development team of Blast software.


### Fix bugs in version 1.423

+ The function of  <b>```Repeat Fragment Search``` </b> cannot work in BioAider V1.423.
+ The <b>```Remove High-Similar sequences```</b> cannot work in BioAider V1.423.
+ The file directory of the main interface cannot be automatically updated in BioAider V1.423.
+ Some bugs on sorftware interface. Optimize interactive operation and beautify the interface.


## BioAider V1.532-beta (Feb 01, 2024)
Compared to BioAider V1.527

### Add new functions

+ Add an extra output file in the ```Combination nt and aa (nt/aa)``` function of <b>```Sequence Identity Matrix```</b>, according to the user's proposed needs. The extra output data was used to draw heatmaps, below the diagonal is nucleotide identity and above diagonal is amino acid identity.

+ In the codon-based function, allow both base T and base U to exist in the input sequence-file, BioAider replaces all base U with base T before the calculation in these sections below,

  + The codon-alignment method based on MAFFT, Muscle and Clustal-Omega plugins.

  + the codon-based options in <b>```Mutation Analysis```</b>, <b>```Sequence Identity Matrix```</b> and <b>```Sequence Vary```</b>(nt → aa translation).
  
  + <b>Tip</b>: still, we want you to import consistent sequences correctly.

+ Change the import method of MAFFT, Muscle, Clustal-Omega and FastTree plugins, the new version using the <b>```Manage plugins``` </b>menu instead of requiring ```external_program.zip```.


### Fix bugs
+ In the previous <b>```Ambiguous Base Edition```</b>, if there is not stop-codon at the end of the sequence, the last three bases will be deleted by mistake. This bug was fixed by the original contributors (Xiyue Wang). 
