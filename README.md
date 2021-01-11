# 16s_cnv_correction_databases

Files prepared from the rrnDB database for use in the copy-number correction of 16S amplicon data. Can be used by stating the folder in the `--ref-dir `
option when using the `place_seqs.py` command of the (Picrust2)[https://github.com/picrust/picrust2/wiki/Sequence-placement] pipeline. 

Afterwards, the 16S.txt file has to be used in the hidden state prediction using `hsp.py` using the `--observed_trait_table` option.
