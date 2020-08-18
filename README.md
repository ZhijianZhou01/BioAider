# Bioinformatics Aider(BioAider)

---

## 1. Introduction
With the development of sequencing technology, a large amount of genomic sequenced datas has been accumulated. Analyzing these data will help us understand their genetic variation at the molecular level. However, processing a large-scale sequences is difficult for biological or clinical expert without bioinformatics and programming skills. Besides,  the needs are also diverse due to different research purposes. Therefore,  simplicity of operation and diversity of function are needed.


BioAider is developed  based on Python3 and R, which is a user-friendly GUI-interface program. As a desktop platform for genomic sequencing data studies, BioAider is designed to simplicity of operation and high summary of analysis results, which could save a lot of time for researchers. 

## 2. Download and install
BioAider and all the updated versions is freely available for non-commercial user at [https://github.com/ZhijianZhou01/BioAider/releases](https://github.com/ZhijianZhou01/BioAider/releases). After obtaining the program, users could directly run the program by clicking executable file without installing in Windows or Linux(Ubuntu 16.04 or more) systerms.


## 3. Example of functions
<b>Note：</b> The BioAider will be in long-term development and functional improvement. We only introduce some functional here, please refer to the instruction manual for details.


### 3.1. Mutation Analysis
This function is used for analysis of the mutations characteristicson on large numbers of sequenced strains. The sequence datas for analysis needs to be aligned in advance, and they could be nucleotides, proteins or simply coding gene fragments. For codon gene, BioAider provides multiple sets of different codon tables, and could scan each condon sites in aligned sequence datasets, and identifies the type of mutation, including synonymous, non-synonymous, insertions and deletions and early termination. Finally, BioAider will automatically summarize and output the relevant analysis results. 

Whether it’s nucleotides or amino acids or coding genes, BioAider could plot the frequency distribution graph for mutation sites through specifing groups of substitution frequencey in custom.

![image.png](https://github.com/ZhijianZhou01/BioAider/raw/master/Figures/Groups_of_mutation_frequency.png)

The each groups of substitution frequencey contains start value and end value which are separated by tab symbol. Note, the start value of each group is not included in the range of frequency.

Then copy them to BioAider

![image.png](https://github.com/ZhijianZhou01/BioAider/raw/master/Figures/Mutation_Analysis.png)
#### 

#### 3.11. Seqformat Convertor
