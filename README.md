# BioAider V1.0

---

## 1. Introduction
With the development of sequencing technology, a large amount of genomic sequenced datas has been accumulated. Analyzing these data will help us understand their genetic variation at the molecular level. However, processing a large-scale sequences is difficult for biological or clinical expert without bioinformatics and programming skills. Besides,  the needs are also diverse due to different research purposes. Therefore,  simplicity of operation and diversity of function are needed.


BioAider is developed  based on Python and R, which is a user-friendly GUI-interface program. As a desktop platform for genomic sequencing data studies, BioAider is designed to simplicity of operation and high summary of analysis results, which could save a lot of time for researchers. 

## 2. Download and install
BioAider V1.0 is freely available at [https://github.com/ZhijianZhou01/BioAider/releases](https://github.com/ZhijianZhou01/BioAider/releases). Currently, the available version is only for windows system. After obtaining the program, users  could directly run the program by clicking BioAider.exe without installing.


## 3. Functions
The functions of BioAider are contained in different sectors.  In general, the input format of the sequence is in fasta. At present, there are 3 functional sectors.

### 3.1. SeqTools
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591953971698-560e16fb-1e29-44e7-ab16-262183f19d7a.png#align=left&display=inline&height=267&margin=%5Bobject%20Object%5D&name=image.png&originHeight=267&originWidth=477&size=17335&status=done&style=none&width=477)

There are 6 sub-menus under the menu bar of the SeqTools Library, which are Seqformat Convertor, SeqVary, SequenceID Rename, Split Sequence Fragmenet, Combine Gene, Visual Gene Extractor and Fast Annotation.
#### 

#### 3.11. Seqformat Convertor
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591954307883-1874d65c-7d37-42a3-955e-ea6a36035639.png#align=left&display=inline&height=237&margin=%5Bobject%20Object%5D&name=image.png&originHeight=237&originWidth=460&size=10087&status=done&style=none&width=460)

This function provides mutual conversion among several common sequence formats, which are Fasta, Nexus, Paml, and Phylip. Of note, the "Data type" option is only available when the target format is "Nexus".


#### 3.12. SeqVary
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591955307265-3eef1b98-4283-492d-aff0-ff49cdb2e615.png#align=left&display=inline&height=345&margin=%5Bobject%20Object%5D&name=image.png&originHeight=345&originWidth=536&size=15353&status=done&style=none&width=536)

The "SeqVary" option of BioAider provides some small functions for sequence preprocessing. "Extract seqTaxon" is used to batch extract sequence names. Note the "DNA_Protein" option requires the gene sequences datas to be aligned based on codons.


#### 3.13. SequenceID Rename
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591957119907-c5a6b746-750e-4fdb-88e2-d0d322905d5d.png#align=left&display=inline&height=489&margin=%5Bobject%20Object%5D&name=image.png&originHeight=489&originWidth=485&size=14759&status=done&style=none&width=485)

This function can rename the original name in sequence datas or tree file etc. In particular, the pictures of the evolutionary tree used for publication often require the taxons of tree to follow a uniform format, so first batch replacement in the tree file saves the trouble of using vector graphics tools to modify later.


#### 3.14. Split Sequence Fragmenet
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591958944595-6dab83a0-4482-486e-9ad4-5177157ac094.png#align=left&display=inline&height=489&margin=%5Bobject%20Object%5D&name=image.png&originHeight=489&originWidth=482&size=17625&status=done&style=none&width=482)

This function can batch intercept the specified range of gene fragments, two different modes are available:  specified different range (Different range) for each sequence, equal range for all sequences (Equal range).

#### 3.15. Combine Gene
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591961596314-a4f9103b-cd54-41eb-bace-3b7659cf8b71.png#align=left&display=inline&height=322&margin=%5Bobject%20Object%5D&name=image.png&originHeight=322&originWidth=472&size=14326&status=done&style=none&width=472)

This function is used to concatenate multiple gene sequences into one. Users can first put different genes dataset files into the same folder, and then drag the folder into the inputbox, then click the  "Load file button"  import the file path of each genes datasets into textbox.  Users can modify the order of genes by manually adjusting the sort of file path in the textbox. Of note, all the sequences should be in fasta format.


#### 3.16. Visual Gene Extractor
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591964885443-e88756cb-7b0c-4e21-bb50-492387a8968c.png#align=left&display=inline&height=534&margin=%5Bobject%20Object%5D&name=image.png&originHeight=534&originWidth=1169&size=67043&status=done&style=none&width=1169)

This function is used to extract the specified gene sequences from mixed coding gene sequence set which was downloaded from NCBI nucleotide database. Given that the same gene may have different manifestations in different studies, the textbox of Gene name could enter multiple names, and BioAider will extract the corresponding gene sequence which contain these gene names.

#### 3.17. Fast Annotation
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591966423576-73566390-d97b-4516-b746-03adb666536d.png#align=left&display=inline&height=493&margin=%5Bobject%20Object%5D&name=image.png&originHeight=493&originWidth=486&size=22456&status=done&style=none&width=486)

For these strain sequences from the same or highly related species, their nucleotide identity is usually relatively higher.  Therefore, the sequences annotation could be based on the gene information of the reference sequence after multi-sequence alignment. BioAider provides a quickly sequence annotation function, users can import the aligned gene sequence set (fasta format file), and adjust the reference sequence for annotation to the forefront of the file. Paste the gene information of reference sequence, name, starting string and end  string into the textbox, separated by ",". Then batch abstract genes. Note that the start string or end string of the gene is not limited in length, but it is required to be unique in the reference sequence. Besides, the higher of  similarity among sequences, the higher accuracy of the annotation.


### 3.2. Similar Analysis
#### 3.2.1 Sequence Identity Matrix
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591968119009-e4ae8114-ab40-484b-97e2-d1b39be6c8f8.png#align=left&display=inline&height=238&margin=%5Bobject%20Object%5D&name=image.png&originHeight=238&originWidth=538&size=11329&status=done&style=none&width=538)

By inputting the aligned sequence datasets in fasta format, and a pairwise sequence identity matrix can be generated. This function contains two different modes: nucleotide or amino acid sequence identity matrix (Single nt or aa), nucleotide plus amino acid sequence identity matrix (Combination nt and aa). It should be noted that if the "Combination nt and aa" is selected, the inputed sequences should be aligned based on codon method.  In order to better fit the variation characteristics , BioAider provides the "Condense gap" function. If  the option was selected, the program will treat every 3 consecutive inserted or deleted bases as one.


#### 3.2.2 Remove H-Similar Sequence
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591968966000-eee9f721-984e-4eed-ac7a-b53e1b3a7534.png#align=left&display=inline&height=273&margin=%5Bobject%20Object%5D&name=image.png&originHeight=273&originWidth=453&size=12017&status=done&style=none&width=453)

This function could remove highly similar sequences and keep one by specifing the threshold of  similarity (Similar threshold). BioAider provides 6 different methods for calculating the similarity of sequences. It should be noted that the "Sequence Identity" and "Hamming" methods require the input sequences data are aligned, and we suggest that the sequences datasets for remaining 4 methods  better not be pre-aligned, because these algorithm own alignment function. If the Similar threshold is seted to 100,  the function of excluding repeated sequences will be turned on.
If you want to obtain the sequence similarity matrix calculated by the above 6 methods, you can click the right button of mouse  in any region of the program interface to call up the functional menu.


### 3.3. Mutation Tools
#### 3.3.1. Mutation Analysis
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591972687015-146b86c9-95a7-4439-8b1e-b647ff0d330d.png#align=left&display=inline&height=403&margin=%5Bobject%20Object%5D&name=image.png&originHeight=403&originWidth=468&size=12496&status=done&style=none&width=468)

This function is used for analying the mutations characteristicson of single or combined coding gene. BioAider will scan each condon sites in aligned sequence datasets, and identifies the type of mutation, including synonymous, non-synonymous, insertions and deletions.  Finally, BioAider will automatically summarize and output the relevant analysis results. It should be noted that the input sequence is required to be pre-aligned based on standard codon method. The each line of Groups of substitution frequencey represents one group of substitution frequencey for synonymous or nonsynonymous sites , and start value and end value are separated by tab symbol. Note, the start value of each group is not included in the range of frequency. Especially, the substitution frequency distribution image is drawn by R program, so you have to make sure the Rscript.exe have been added into BioAider throung the plugin function.


#### 3.3.2. Site Counter
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591973882816-74679876-c118-4d73-ae9d-31ce37ae28e8.png#align=left&display=inline&height=278&margin=%5Bobject%20Object%5D&name=image.png&originHeight=278&originWidth=530&size=12526&status=done&style=none&width=530)

This function could summary the type, count and proportion of bases (or amino acids) at each site for the aligned sequence datasets. In addition, BioAider will output a consensus sequence based on the highest proportion base (or amino acid) in each site.


#### 3.3.3. Site Scree
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591974422038-23e76bd4-9c08-45e1-8787-a44b46e0fff2.png#align=left&display=inline&height=328&margin=%5Bobject%20Object%5D&name=image.png&originHeight=328&originWidth=482&size=9156&status=done&style=none&width=482)

This function is used to extract the sequences with corresponding base or amino acid in specified one or more site. It is very useful for studying whether there is linkage inheritance among different gene sites.


### 3.4 Plugin
![image.png](https://cdn.nlark.com/yuque/0/2020/png/119869/1591975870669-db32d067-1180-40b2-b6e4-a595f809d845.png#align=left&display=inline&height=143&margin=%5Bobject%20Object%5D&name=image.png&originHeight=143&originWidth=456&size=7236&status=done&style=none&width=456)

BioAider opens the plug-in function, users can add executable programs into BioAider by click the menu bar of Manage  Packages and select Add packages.



