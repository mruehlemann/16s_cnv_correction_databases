# 16s_cnv_correction_databases

Files prepared from the rrnDB database for use in the copy-number correction of 16S amplicon data. Can be used by stating the folder in the `-r `
option when using the `place_seqs.py` command of the [Picrust2](https://github.com/picrust/picrust2/wiki/Sequence-placement) pipeline. 

Example:
```
place_seqs.py -s study_seqs.fna -o placed_seqs.tre -p 1 -r /path/to/16s_cnv_correction_databases/rrnDB-5.6_RAXML
```

Afterwards, the 16S.txt.gz file has to be used in the hidden state prediction using `hsp.py` using the `--observed_trait_table` option.
```
hsp.py -t placed_seqs.tre -o marker_nsti_predicted.tsv.gz -p 1 -n --observed_trait_table /path/to/16s_cnv_correction_databases/16S.txt.gz
```

Both datasets use the same sequences, however the trees for sequence placement were inferred using different software (iqtree and raxml-ng).
