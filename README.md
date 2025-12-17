# COVID-19-vacc-gwas

Code and data related to "Genetic variation in HLA, IGKV and HHEX loci influence mRNA vaccine-induced long-lasting humoral protection against COVID-19"

🔗 Preprint: https://www.medrxiv.org/content/10.1101/2025.10.21.25337971v1

# Data availability

## Per-cohort GWAS summary statistics:

GWAS Catalog ID: GCP001506

[GWAS of anti-S antibody concentrations after two COVID-19 vaccinations (RisCoin cohort)](http://ftp.ebi.ac.uk/pub/databases/gwas/summary_statistics/GCST90726001-GCST90727000/GCST90726556)

[GWAS of anti-S antibody concentrations after three COVID-19 vaccinations (RisCoin cohort)](http://ftp.ebi.ac.uk/pub/databases/gwas/summary_statistics/GCST90726001-GCST90727000/GCST90726557)

[GWAS of live-virus neutralization activity after two COVID-19 vaccinations (RisCoin cohort)](http://ftp.ebi.ac.uk/pub/databases/gwas/summary_statistics/GCST90726001-GCST90727000/GCST90726558)

[GWAS of live-virus neutralization activity after three COVID-19 vaccinations (RisCoin cohort)](http://ftp.ebi.ac.uk/pub/databases/gwas/summary_statistics/GCST90726001-GCST90727000/GCST90726559)

[GWAS of anti-S antibody concentrations after two COVID-19 vaccinations (KoCo19 cohort)](http://ftp.ebi.ac.uk/pub/databases/gwas/summary_statistics/GCST90726001-GCST90727000/GCST90726560)


## GWAS meta-analysis summary statistics and per-cohort HLA-was summary statistics
`wget https://github.com/kimhellmuthlab/COVID-19-vacc-gwas/releases/download/submission/data_availability.zip`

# Main Analysis steps

## Software environment:
You can pull the singularity container from

`singularity pull oras://community.wave.seqera.io/library/bcftools_gemma_plink2_plink:4af92dd501f3810e`

## Genotype QC

Adjust `Snakefile_genoQC` and run using snakemake i.e. `snakemake -j 1 -s Snakefile_genoQC`

## Association analysis

Adjust `Snakefile_association` and run using snakemake i.e. `snakemake -j 1 -s Snakefile_association`
