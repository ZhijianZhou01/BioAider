# Bioinformatics Aider (BioAider)

## Releases: https://github.com/ZhijianZhou01/BioAider/releases

## Latest version: BioAider V1.423 (Mar 24, 2022)


## Revision history:
### BioAider V1.0 (May 27, 2020)
The first version of BioAider V1.x.

----
### BioAider V1.03 (Jul 22, 2020)
1. Rewrite and beautify the interface of program by PySide2, add more prompts for controls.
2. Add a Linux dsitribution (GUI) for Ubuntu (16.04 and more) users.
Packed three popular multiple-sequence alignment tools(MAFFT, Muscle, Clustal-Omega) and provide graphical interfaces. What's more, provide translation-alignment for codon gene.
3. Added multiple sets of codon table in multiple-sequence alignment and in features of “Mutation analysis”.
4. Add variation analysis of non-coding gene and amino acid sequence in features of “Mutation analysis”.
5. Increased the pop-up window of program bug and toolbar for some common features.
Add some new other features and fixed some bugs.

---
### BioAider V1.314 (Sep 2, 2020)
1. Add the feature of looking for repetitive fragments.
2. Add the feature of locating the protein to the nucleotide sequence.

---
### BioAider V1.334 (Mar 28, 2021)
1. Add the following functions:
    (1) Viral *.gb file parser: Extract the information from virus *.gb file, such as host, collection date and country, reference article, etc. What's more, BioAider can be extracted and stored according to species relationship;
    (2) Ambiguous Base Edition: Processing ambiguous bases and premature stop codons (preparing sequences for PAML analysis);
    (3) Delete Low-Similar Sequence: Removing sequences with similarity below the threshold:
    (4) FastTree: Graphical interface of FastTree software, which is suitable for big data;
    (5) Date converted to Decimal: Convert date to decimal;
    (6) Sequence Batch Download (NCBI): NCBI sequence batch search;
    (7) File Merge: Simple function of combining multiple files into one file:
    (8) Increased the output linked mutation sites and re-beautified the mapping in Mutation analysis function.

2. Fix bugs
    (1) Mutation Analysis function: Fixed the bug that the "number of stop codons" cannot be counted in the summary file;
    (2) Other bugs

Please pay special attention:
On April 24, 2021 (International Veterinary Day), we uploaded the BioAider distribution for MacOS system for the first time, and fixed some bugs in the last uploaded windows and linux version (but keep the version number 1.334 unchanged).

---
### BioAider V1.423 (Mar 24, 2022)
#### Fix bugs
1. (Important) the output result of "Codon method" in mutations analysis.
  1.1. Resolved the bug that could not correctly plot the frequency distribution of synonymous and non-synonymous substitution sites using "base" as the statistical unit (the result of "_substitution frequency distribution.pdf" and "_single syn or non-syn substitution nt sites.csv" and "*_Frequency group of sys and non-sys substitution.txt") when there are a large number of different kinds of mutations at the same codon site (e.g. sequences are from different genera or species, or large number of dinucleotide and trinucleotide substitution sites). Note that even if this bug is resolved, it is not recommended to apply it to the sequence sets with a large variety of variants at the same codon site, because it maybe no real value to count the number of nucleotides sites based on mutation frequency.
    Tip：Statistical results (such as *_all site.csv and *_mutation site.csv) using "codons" as units are fine for any sequences in the previous version.

  1.2. Resolved the bug that incorrect count of nt in "Others information" part in the end of "_mutation site summary.txt" when there are a large number of dinucleotide and trinucleotide substitution sites in sequence sets.
    Tip：Except for the "Others information" part, everything else in "_mutation site summary.txt" is correct in the previous version.

2. Solved the problem that "Delete Lower similar sequences" cannot run in BioAider v1.334.

3. The problem that the input file or directory cannot contain "."

#### Add new functions
1. <b>(New and important)</b> Optimized algorithm to greatly speed up BioAider, and quickly perform mutation analysis on hundreds of thousands of pieces of data (2022/03/24).

2. "Codon" method of mutation analysis add the option to delete "nt sites with both synonymous and nonsynonymous substitution" freely when drawing the graph of "frequency distribution of synonymous and non-synonymous substitution sites".

3. (New and important) Function for drawing a lollipop map of gene (or genome) mutation sites.

4. Function to draw scatter,boxplots, violin diagram for data based on seaborn package (GUI interface).

5. Function to switch various themes freely.

---

