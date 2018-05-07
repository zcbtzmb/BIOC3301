# BIOC3301 Data Analysis Code
Please open the BIOC3301 folder to find all of the code used for the analysis of the Illumina sequencing data. 

## Workflow 

1. Join_paired_ends_script.pbs - This script joines the Read1 and Read2 fastq files for the 2018 dataset. This script was not performed on the 2016 and 2017 datasets due to poor Read2 quality. 

2. Demultiplexing_script.pbs, Demultiplexing_2017.pbs, Demultiplexing_2016.pbs - Demultiplexed the 2018, 2017 and 2016 datasets respectively.

3. Picking_OTUs_2018.pbs, Picking_otus_2017.pbs, Picking_otus_2016.pbs - Using the SILVA reference database, OTUs were assinged to each of the datasets. 

4. Remove_Samples.pbs - Two samples were removed from the 2018 dataset as these samples were not collected from Gordon Square Gardens.

5. Merge_otus_all.pbs - The OTU tables for each dataset were merged together. 

6. Diversity_Analysis_merged.pbs - Core Diversity Analysis workflow was ran for the merged OTU table. 

7. Compute_core_microbiome_2018.pbs, Compute_core_microbiome_2017.pbs, Compute_core_microbiome_2016.pbs - The OTU tables of each dataset were used to select a core OTU table of differing levels. 90% cut off was selected.

8. Merge_core_otu_table_90.pbs - The core OTU tables for each dataset were merged together. 

9. Divesity_Analysis_merged_core_90.pbs - Core Diversity Analysis workflow was ran for the merged core OTU table. 

10. Summarize_taxa_merged_core_90.pbs - The OTU table was summarised at the level of phyla. 

11. make_heat_map_merged_core_90.pbs - Generated a heat map showing the relative abundance of phyla in all the samples. 

12. jackknifed_beta_diversity.pbs - Generated weighted UniFrac distances and repeatedly resampled a subset of data for each sample to test the robustness of clustering. 

13. Adonis_weighted_core.pbs, Anosim_weighted_core.pbs - Statistical tests of beta diversity. 

14. Group_significance_core_KW_90.pbs - KW statistical test of alpha diversity. 

15. split_merged_otu_table_90_L2.pbs - Splitting the merged core OTU table into phyla. 

16. Proteobacteria_diversity_analysis.pbs - Core Diversity Analysis workflow was ran for the Proteobacteria phylum. 

17. Adonis_weighted_proteobacteria.pbs, Anosim_weighted_proteobacteria.pbs - Statistical tests of beta diversity within the Proteobacteria phylum. 

18. Summarize_taxa_90_proteobacteria_L3.pbs - Classes were summarised within the proteobacteria phylum. 

19. Group_significance_core_KW_Proteobacteria_L3.pbs - KW statistical test of alpha diversity was ran for the Proteobacteria classes. 
