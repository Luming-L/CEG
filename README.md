# Introduction
In evolutionary biology, "supermatrix" is a data matrix used to reconstruct genome phylogeny, which contains multiple sequence alignments (MSA) of multiple genes. 

A possible workflow for building supermatrix:

 1. Find ‘universal single-copy’ orthologues across the taxonomic group ([OrthoFinder](https://github.com/davidemms/OrthoFinder) and [Batch Web CD-Search Tool with Pfam database](https://www.ncbi.nlm.nih.gov/Structure/bwrpsb/bwrpsb.cgi)).
 2. Make a multiple alignment of each orthogroup, respectively ([MAFFT](https://mafft.cbrc.jp/alignment/software/)).
 3. Concatenate the alignments. The length of one concatenated alignment is the sum of each orthogroup's MSA length.

(Barker, D 2020, _Lecture 4: Phylogeny_, lecture notes, Comparative and Evolutionary Genomics PGBI11115, The University of Edinburgh, delivered Feb 2020.)
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
```
python3 MakeSupermatrix.py MSAfileNames.txt
```put
stop_calc=0, 
seq='', 
ohdis = 1 - tick "粘端差异>1"; ohdis = 0 - not tick "粘端差异>1"
simbase = 1 - tick '粘端~1'; simbase = 0 - not tick '粘端~1'. '粘端~1' means '允许粘端差异=1, 但差别必须是嘧啶对嘌呤, 如AATC-ATTC').
wrap_let=['[\'AGG\', [4, 7]]','[\'ACC\', [-7, -4]]'] - [5'Wrap, 3'Wrap]. 5'Wrap and 3'Wrap will be added to the 5' and 3' ends of original A/B/C...(about 200bp).
plen=60 - 'Len of oligo<'
pno=6.0 - 'Group size: '
bipar=0 - 'Group size: '
qua=(0.7, -1.5, -5,  6,  18) - Quality Default
onebyonemode=False, 
elist='' - Avoid list of sticky ends
danres='' - 'Warning list of strings' wrap mode
btsiwrap=True -  self.rb_btsi.get_active() - 'Oligo Wrapping:'
dataQueue=None
specific='' - "Specific"
ligvalue=1 - self.cbligv.get_active() - '连值'，'将连接判断加入设计, 即考虑被连接端靠近粘端的5个碱基组成.'
cutvalue=1 - self.cbcutv.get_active() - '切值'，'将酶切判断加入设计, 即考虑连接端靠近粘端的几个碱基.'
endtolerate=0 - self.cbendtolerate.get_active()
tolvalue=0 - self.entryendtolerate.get_text() - '宽边' - '如果确定, 则允许第一条和最后一条引物的二级结构更松一些, 这样可能有利于二次拼接' - '只有在宽边被选择时有效, 这个数值是第一条和最后一条比其它引物deltaG的高出数值, 比如其它引物deltaG差值是10, 则第一条和最后一条可以使6'
filtervalue=0 - filtervalue - '简化计算'
vecsticklen=3 - self.vecstickylen
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTAxNTQ3Nzk5NywtNTIyNzg1ODA1LDE2OD
cxNTgzMjQsLTExNDA4NzI0MzksLTE1NTc1NTc2ODksLTQ2NDU3
NTA1MiwtMTEyODQ4ODQ0Ml19
-->