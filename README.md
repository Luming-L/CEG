# Introduction
In evolutionary biology, "supermatrix" is a data matrix used to reconstruct phylogeny. method concatenates sequences from multiple genes into a data supermatrix for phylogenetic analysis
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
eyJoaXN0b3J5IjpbMTk3MDU2OTgzNiwtNDY0NTc1MDUyLC0xMT
I4NDg4NDQyXX0=
-->