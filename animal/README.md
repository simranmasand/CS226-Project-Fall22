# Various animals/organisms genotype phenotype data

|       | Samples | SNPs | Phenos | misc. |
|:-----:|:-------:|:----:|:------:|:-----:|
| Mouse |   55    | 421k |  120   |   Up to 10 clones per strain (genotype)    |
| Wheat |   504   | 20k  |   71   |      |
| Yeast |    1008 | 11k  |   46   |       |


## Mouse

Mouse phenotype and genotype data was obained from the mouse phenome database [https://phenome.jax.org](https://phenome.jax.org).

The data specifically involves population "BXD" which was genotyped and phenotyped in relation to study "Auwerx1" [https://phenome.jax.org/projects/Auwerx1](https://phenome.jax.org/projects/Auwerx1). The study involved up to 10 clones of one genotyped mouse who received varying treatment, such that there are multiple phenotypes available per genotype.

To make the pairings between genotypes and phenotypes clear, the first column in the genotype files (delimited by comma) is the strain ID which should match up with the strain identifier in the phenotype file.

## Wheat

Obtained from [http://mtweb.cs.ucl.ac.uk/mus/www/MAGICdiverse/](http://mtweb.cs.ucl.ac.uk/mus/www/MAGICdiverse/).

The 55k LD Pruned sites were downloaded and filtered to ~20k with no missing genotypes. The data is haploid, such that there are only two possibilities per SNP (indicated using 0s and 1s).

The genotype file was generated using Plink2
```
./plink2 --bfile MAGIC_PLINK_PRUNED/ALLchr.SNPs.pruned --export A --out wheat_additive
```

Phenotype information was obtained from [https://doi.org/10.1101/2020.09.15.296533](https://doi.org/10.1101/2020.09.15.296533).

Phenotypes were reportedly measured in year 1 and year 2  (`_1` or `_2` prefix) for many phenotypes and more frequently (up to to 10 times) for some phenotypes.

More information on each phenotype can be found in the paper.

## Yeast

Obtained from [http://genomics-pubs.princeton.edu/YeastCross_BYxRM/home.shtml](http://genomics-pubs.princeton.edu/YeastCross_BYxRM/home.shtml).

Similar to the Wheat data, the Yeast data is also haploid, such that each SNP is one of two possibilities (indicated with 0s and 1s).

More information about this data can be found in the paper [http://www.nature.com/nature/journal/v494/n7436/full/nature11867.html](http://www.nature.com/nature/journal/v494/n7436/full/nature11867.html)

