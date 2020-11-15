# Introduction
In evolutionary biology, "supermatrix" is a data matrix used to reconstruct genome phylogeny, which contains multiple sequence alignments of multiple genes. 

A possible workflow for building supermatrix:

 1. Find ‘universal single-copy’ orthologues across the taxonomic group.
 2. Make a multiple alignment of each orthogroup, separately.
 3. 

 
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
eyJoaXN0b3J5IjpbLTIxMjE2NjQ0ODUsLTQ2NDU3NTA1MiwtMT
EyODQ4ODQ0Ml19
-->