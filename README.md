# Bioinformatics Aider (BioAider)


## 1. Introduction
With the development of sequencing technology, a large amount of genomic sequenced datas has been accumulated. Analyzing these data will help us understand their genetic variation at the molecular level. However, processing a large-scale sequences is difficult for biological or clinical expert without bioinformatics and programming skills. Besides,  the needs are also diverse due to different research purposes. Therefore,  simplicity of operation and diversity of function are needed.

BioAider is developed  based on Python3 and R, which is a user-friendly GUI-interface program. As a desktop platform for genomic sequencing data studies, BioAider is designed to simplicity of operation and high summary of analysis results, which could save a lot of time for researchers. 

## 2. Download and install
BioAider and all the updated versions is freely available for non-commercial user at [https://github.com/ZhijianZhou01/BioAider/releases](https://github.com/ZhijianZhou01/BioAider/releases). After obtaining the program, users could directly run the program by clicking executable file without installing in Windows or Linux(Ubuntu 16.04 or more) systerms.

## 3. Example of functions
<b>Note：</b>BioAider will be in long-term development and functional improvement in the future. We only introduce some functional here, please refer to the instruction manual for details.

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

![SARS-CoV-2_ORF3a_aligned_summary_file.png](https://github.com/ZhijianZhou01/BioAider/raw/master/Figures/Mutation_analysis_codon_sequence_summary_file.png)

You could also konw the number of mutation sites under each mutation frequency group through view <b>*_substitution frequency distribution.png</b>:

![SARS-CoV-2_ORF3a_aligned_substitution frequency distribution.png](https://github.com/ZhijianZhou01/BioAider/raw/master/Figures/SARS-CoV-2_ORF3a_aligned_substitution_frequency_distribution.png)
 
It is not difficult to find that more than half of the mutation sites only appear in a single strain, although there are many mutation sites in ORF3a gene.

Or could obtain the corresponding mutant strain of these variant sites in the detailed <b>*_log.txt</b> file:

![SARS-CoV-2_ORF3a_aligned log.png](https://github.com/ZhijianZhou01/BioAider/raw/master/Figures/Mutation_analysis_codon_sequence_log.png)

### 3.2. Fast Annotation
For these strain sequences from the same or highly related species, their nucleotide identity is usually relatively higher. Therefore, the sequences annotation could be based on the gene information of the reference sequence after multi-sequence alignment. 

BioAider provides a quickly sequence annotation function, users can import the aligned gene sequence set (fasta format file), and adjust the reference sequence for annotation to the forefront of the file. Paste the gene information of reference sequence, name, starting string and end  string into the textbox, separated by ",". Then batch abstract genes. Note that the start string or end string of the gene is not limited in length, but it is required to be unique in the reference sequence. Besides, the higher of  similarity among sequences, the higher accuracy of the annotation.

![Fast_Annotation.png](https://github.com/ZhijianZhou01/BioAider/raw/master/Figures/Fast_Annotation.png)

### 3.3. Sequence Identity Matrix
This function contains two different modes: nucleotide or amino acid sequence identity matrix (Single nt or aa), nucleotide plus amino acid sequence identity matrix (Combination nt and aa). It should be noted that if the "Combination nt and aa" is selected, the inputed sequences should be aligned based on codon method. 

In order to better fit the variation characteristics , BioAider provides the "Condense gap" function. If  the option was selected, the program will treat every 3 consecutive inserted or deleted bases as one.

![Sequence_Identity_Matrix.png](https://github.com/ZhijianZhou01/BioAider/raw/master/Figures/Sequence_Identity_Matrix.png)

### 3.4. Seqformat Convertor
BioAider provides mutual conversion among several common sequence formats, which are Fasta, Nexus, Paml, and Phylip. Of note, the "Data type" option is only available when the target format is "Nexus".

![Seqformat_Convertor.png](https://github.com/ZhijianZhou01/BioAider/raw/master/Figures/Seqformat_Convertor.png)


## 4. Test Datas
![https://github.com/ZhijianZhou01/BioAider/tree/master/Example](https://github.com/ZhijianZhou01/BioAider/tree/master/Example)

## 5. Bug report
![GitHub issue](https://github.com/ZhijianZhou01/BioAider/issues) or send email to zjzhou@hnu.edu.cn.
