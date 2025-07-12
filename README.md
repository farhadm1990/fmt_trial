# A repo summplementary to FMT trial

# 1. System requirements:

Operating system: Linux Ubuntu 22.04 LTS was used for the analysis.


# Recourse requirement


| Job type            | CPUs     | Memory (Gb) |
|--------------------|-------------|------------|
| Atlas pipline	             | 40    | 150 |
| R workflow             | 8    | 16 |

# 2. Versions for all softwares used


| Package            | Version     | Repository |
|--------------------|-------------|------------|
| Python             | 3.10.12     | [python/cpython](https://github.com/python/cpython) |
| metagenomics-atlas | 2.18.2      | [metagenome-atlas/atlas](https://github.com/metagenome-atlas/atlas) |
| R                  | 4.4.1       | [wch/r-source](https://github.com/wch/r-source) |
| phytools           | 2.3-0       | [liamrevell/phytools](https://github.com/liamrevell/phytools) |
| tidytree           | 0.4.6       | [YuLab-SMU/tidytree](https://github.com/YuLab-SMU/tidytree) |
| yaml               | 2.3.10      | [yaml/pyyaml](https://github.com/yaml/pyyaml) |
| arrow              | 17.0.0.1    | [apache/arrow](https://github.com/apache/arrow) |
| ggtree             | 3.12.0      | [YuLab-SMU/ggtree](https://github.com/YuLab-SMU/ggtree) |
| kableExtra         | 1.4.0       | [haozhu233/kableExtra](https://github.com/haozhu233/kableExtra) |
| useful             | 1.2.6.1     | [jbryer/useful](https://github.com/jbryer/useful) |
| vegan              | 2.6-8       | [vegandevs/vegan](https://github.com/vegandevs/vegan) |
| ape                | 5.8         | [emmanuelparadis/ape](https://github.com/emmanuelparadis/ape) |
| pheatmap           | 1.0.12      | [raivokolde/pheatmap](https://github.com/raivokolde/pheatmap) |
| ggbeeswarm         | 0.7.2       | [eclarke/ggbeeswarm](https://github.com/eclarke/ggbeeswarm) |
| ggrepel            | 0.9.6       | [slowkow/ggrepel](https://github.com/slowkow/ggrepel) |
| heatmaply          | 1.5.0       | [talgalili/heatmaply](https://github.com/talgalili/heatmaply) |
| viridis            | 0.6.5       | [sjmgarnier/viridis](https://github.com/sjmgarnier/viridis) |
| plotly             | 4.10.4      | [plotly/plotly.py](https://github.com/plotly/plotly.py) |
| glue               | 1.8.0       | [tidyverse/glue](https://github.com/tidyverse/glue) |
| phyloseq           | 1.48.0      | [joey711/phyloseq](https://github.com/joey711/phyloseq) |
| tidyverse          | 2.0.0       | [tidyverse/tidyverse](https://github.com/tidyverse/tidyverse) |


# 3. Installation guide

```sh

mamba install -c bioconda -c conda-forge metagenome-atlas=2.18.2

# this takes about 5 min to be completed on desktop computers
```

# 4. Instruction to run the demo data

```sh
atlas init --db-dir database demo_data/ -w output --threads 8

tlas run all  --jobs 8  -w ./output -c ./output/config.yaml --keep-going

```

# 5. Expected output

```sh
## Expected outputs from ATLAS

taxonomy_file = "gtdb_taxonomy.tsv"
tree_file  =  "gtdbtk.bac120.nwk"
tree_arch = "gtdbtk.ar53.nwk"
quality_file = "genome_quality.tsv"
counts_file = "counts_genomes.parquet"
abundance_file =  "median_coverage_genomes.parquet"
readstats_file =  "read_counts.tsv"
keggmodules_file = "kegg_modules.tsv"
dram= "dram_annotations.tsv"
dram_xlsx = "metabolism_summary.xlsx"
gene2genomes= "gene2genome.parquet"
bin2genome = "allbins2genome.tsv"

# Gene catalog
coverage_stats = "Genecatalog/counts/gene_coverage_stats.parquet"
coverage = "Genecatalog/counts/median_coverage.h5"
counts = "Genecatalog/counts/Nmapped_reads.h5"
sample_stats = "Genecatalog/counts/sample_coverage_stats.tsv"
geneinfo = "Genecatalog/clustering/orf_info.parquet"
eggnog = "Genecatalog/annotations/eggNOG.parquet"
kegg = "Genecatalog/annotations/dram/kegg.parquet"
cazy = "Genecatalog/annotations/dram/cazy.parquet" 
pfam = "Genecatalog/annotations/dram/pfam.parquet"



```

# 6. Instructions on statistical analysis in R

### A detailed instruction can be found in this ![markdown]() file. 