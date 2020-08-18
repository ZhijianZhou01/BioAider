# Bioinformatics Aider (BioAider)


## 1. Introduction
With the development of sequencing technology, a large amount of genomic sequenced datas has been accumulated. Analyzing these data will help us understand their genetic variation at the molecular level. However, processing a large-scale sequences is difficult for biological or clinical expert without bioinformatics and programming skills. Besides,  the needs are also diverse due to different research purposes. Therefore,  simplicity of operation and diversity of function are needed.

BioAider is developed  based on Python3 and R, which is a user-friendly GUI-interface program. As a desktop platform for genomic sequencing data studies, BioAider is designed to simplicity of operation and high summary of analysis results, which could save a lot of time for researchers. 

## 2. Download and install
BioAider and all the updated versions is freely available for non-commercial user at [https://github.com/ZhijianZhou01/BioAider/releases](https://github.com/ZhijianZhou01/BioAider/releases). After obtaining the program, users could directly run the program by clicking executable file without installing in Windows or Linux(Ubuntu 16.04 or more) systerms.

## 3. Example of functions
<b>Note：</b> The BioAider will be in long-term development and functional improvement. We only introduce some functional here, please refer to the instruction manual for details.

### 3.1. Mutation Analysis
This function could be used for analysis of the <b>mutations characteristicson on large numbers of sequenced strains</b>. The sequence datas for analysis needs to be aligned in advance, and they could be nucleotides, proteins（amino acid） sequences or simply coding gene fragments. For nucleotides and proteins sequences, BioAider could summarizes all the mutation sites with corresponding frequency and strains. 

Of course, if the datas is codon gene, BioAider provides multiple sets of different codon tables for users, and could scan each condon sites in aligned sequence datasets, and identifies the type of mutation, including synonymous, non-synonymous, insertions and deletions and early termination. Finally, BioAider will automatically summarize and output the relevant analysis results.

<b>Note: </b>The codon gene sequences for mutations analysis have to be aligned by translation-alignment methon in advance, It is worth mentioning that BioAider packed three multiple-sequence-alignment software (mafft, muscle and clsutal-omega) in the graphical interface, and and provided translation-alignment additionally.

Whether it’s nucleotides or amino acids or coding genes, BioAider could plot the frequency distribution graph for mutation sites through specifing groups of substitution frequencey in custom.

Eaxmple of mutations analysis for aligned SARS-CoV-2 ORF3a gene sequences. First, create frequency grouping in a table editor:

![Groups of mutation frequency.png](https://github.com/ZhijianZhou01/BioAider/raw/master/Figures/Groups_of_mutation_frequency.png)

The each groups of substitution frequencey contains start value and end value which are separated by tab symbol. <b>Note, the start value</b> of each group is not included in the range of frequency.

Then copy them to the textedit box of BioAider,and select "Codon" single button in "Datas type":

![Mutation Analysis.png](https://github.com/ZhijianZhou01/BioAider/raw/master/Figures/Mutation_Analysis.png)

 After the run is over, these analysis result could be found in the directory where the source file is located, you could scan the <b>*_mutation site summary</b> file then know the overall variation and mutation hotspots.

![Mutation analysis of codon sequence summary file.png](https://github.com/ZhijianZhou01/BioAider/raw/master/Figures/Mutation_analysis_codon_sequence_summary_file.png)

Or obtain the mutant strain of these variant sites in <b>*_log.txt</b> file:

![Mutation analysis codon sequence log.png](https://github.com/ZhijianZhou01/BioAider/raw/master/Figures/Mutation_analysis_codon_sequence_summary_file.png)


#### 

