# Introduction
In evolutionary biology, "supermatrix" is a data matrix used to reconstruct genome phylogeny, which contains multiple sequence alignments (MSA) of multiple genes. 

A possible workflow for building supermatrix:

 1. Find ‘universal single-copy’ orthologues across the taxonomic group ().
 2. Make a multiple alignment of each orthogroup, respectively.
 3. Concatenate the alignments. The length of one concatenated alignment is the sum of each orthogroup's MSA length.

(Barker, D 2020, _Lecture 4: Phylogeny_, lecture notes, Comparative and Evolutionary Genomics PGBI11115, The University of Edinburgh, delivered 21 May 2020.)
# Requirements
 - Python 3
 - Bio
 - sys
# Input
 - several MSA(Multiple sequence alignments) files of orthogroups/genes, check `OG0000296ID_aligned.fa` and `OG0000298ID_aligned.fa` in `MSA/testFiles/Input` as an example.
- a file stores names of all MSA files, check `MSAfileNames.txt` in `MSA/testFiles/Input` as an example.
# Output
 - the supermatrix, like `supermatrix.fa` in `MSA/testFiles/Output`.
# Command
```python
python3 MakeSupermatrix.py MSAfileNames.txt
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2MzE2Mzc4ODAsLTExNDA4NzI0MzksLT
E1NTc1NTc2ODksLTQ2NDU3NTA1MiwtMTEyODQ4ODQ0Ml19
-->