# How to add new genome to work with sicer in galaxy

- make sure you have the genome dbkey of your interest in: /opt/galaxy/tool-data/shared/ucsc/builds.txt 
- Then, you need to update GenomeData.py in ~/SICER/lib/.  For example, adding PlasmoDB_32_PbergheiANKA_Genome requires:

```
PlasmoDB_32_PbergheiANKA_Genome_chroms = ['PbANKA_01_v3', 'PbANKA_02_v3', 'PbANKA_03_v3', 'PbANKA_04_v3',
                                          'PbANKA_05_v3', 'PbANKA_06_v3', 'PbANKA_07_v3', 'PbANKA_08_v3',
                                          'PbANKA_09_v3', 'PbANKA_10_v3', 'PbANKA_11_v3', 'PbANKA_12_v3',
                                          'PbANKA_13_v3', 'PbANKA_14_v3', 'PbANKA_00_v3_archived_contig_1',
                                          'PbANKA_00_v3_archived_contig_2', 'PbANKA_00_v3_archived_contig_3',
                                          'PbANKA_00_v3_archived_contig_4', 'PbANKA_00_v3_archived_contig_5',
                                          'PbANKA_API_v3', 'PbANKA_MIT_v3']

PlasmoDB_32_PbergheiANKA_Genome_chrom_lengths = {'PbANKA_01_v3':515659, 'PbANKA_02_v3':622508,'PbANKA_03_v3':659512,
                                                 'PbANKA_04_v3':712327, 'PbANKA_05_v3':931174, 'PbANKA_06_v3':984266,
                                                 'PbANKA_07_v3':846620, 'PbANKA_08_v3':1420537, 'PbANKA_09_v3':1633586,
                                                 'PbANKA_10_v3':1640193, 'PbANKA_11_v3':1762642, 'PbANKA_12_v3':1807262,
                                                 'PbANKA_13_v3':2521873, 'PbANKA_14_v3':2549703, 'PbANKA_00_v3_archived_contig_1':56810,
                                                 'PbANKA_00_v3_archived_contig_2':34265, 'PbANKA_00_v3_archived_contig_3':24479,
                                                 'PbANKA_00_v3_archived_contig_4':10286, 'PbANKA_00_v3_archived_contig_5':6544,
                                                 'PbANKA_API_v3':34403, 'PbANKA_MIT_v3':5957}


species_chroms = {'mm8':mm8_chroms,
                        'mm9':mm9_chroms,
                        'hg18':hg18_chroms,
                        'hg19':hg19_chroms,
                        "dm2":dm2_chroms,
                        "dm3":dm3_chroms,
                        "sacCer1":sacCer1_chroms,
                        "pombe":pombe_chroms,
                        *"PlasmoDB-32_PbergheiANKA_Genome":PlasmoDB_32_PbergheiANKA_Genome_chroms*,
                        'rn4':rn4_chroms,
                        'tair8':tair8_chroms,
                        'background':background_chroms};

species_chrom_lengths={'mm8':mm8_chrom_lengths,
                       'mm9':mm9_chrom_lengths,
                       'hg18':hg18_chrom_lengths,
                       'hg19':hg19_chrom_lengths,
                       'dm2':dm2_chrom_lengths,
                       'dm3':dm3_chrom_lengths,
                       'sacCer1':sacCer1_chrom_lengths,
                       'pombe':pombe_chrom_lengths,
                       *'PlasmoDB-32_PbergheiANKA_Genome':PlasmoDB_32_PbergheiANKA_Genome_chrom_lengths*,
                       'rn4':rn4_chrom_lengths,
                       'tair8':tair8_chrom_lengths,
                       'background':background_chrom_lengths};

```
