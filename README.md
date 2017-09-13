# FImpute

Instructions, help, and examples related to FImpute imputation software

# About

FImpute was written at the University of Guelph by Mehdi Sargolzaei, Jacques Chesnais, and Flavio Schenkel. FImpute is written to impute genotypes from low-density (e.g. 10k) to high-density (e.g. 50k or 700k). You can also use this to simply impute missing genotypes even if they are all from the same chip. 

# Getting started

First visit their website ([here](http://www.aps.uoguelph.ca/~msargol/fimpute/) and download the Linux version (looks to be the only one available now). 

Once downloaded, I like to put this in my `~/bin/FImpute` folder or you can just put in your `~/bin/` folder (if your `.bashrc` or `.bash_profile` does not have this folder in it's PATH variable, you need to add by adding:

```bash
export PATH=$HOME/bin/FImpute:$PATH
```
or
```bash
export PATH=$HOME/bin:$PATH
```

This will allow your system to find the binaries. 

Also please change the permissions on the program like always in Linux. 

```bash
chmod 775 FImpute
```

# Documentation

You can find the full documentation on the program is online at the website above. Please download and read for full information and all the options available. 

# vim users

I have written vim syntax highlighting files for this program. This could potentially save you very severe problems with imputation by not finding options or entering the wrong word. If it's not on GitHub contact me and I can get you the files and how to install it on your Linux system. 

# File formats

I simply use space delimited files for all input files. 

## Map File

The map file needs (1) SNP name, (2) Chromosome Number, (3) BP Position, (4) Chip position. 

The confusing part is adding the chip position. This example only has 1 chip, but with more chips the position of number 1 will change. For instance, if the first chip contains all SNP, number 1 will start with the first SNP to n of the last SNP. Chip 2 may be a low-density panel and number 1 will start at SNP 10 for example. This will change based on the panels you have. I believe 0 is missing (not on that chip). 

![Screenshot of Map File](/Screenshots/MapFile.png?raw=true "Map file example")

## Genotype File

The genotype file needs (1) ID, (2) Chip Number, (3) Genotypes (0,1,2,5=missing). No spaces in the genotypes (saves lots of space). 

![Screenshot of Genotype File](/Screenshots/GenotypeFile.png?raw=true "Genotype file example")

## Pedigree File

You need a file with (1) Animal ID, (2) Sire, (3) Dam, (4) Sex (M/F). 

![Screenshot of Pedigree File](/Screenshots/PedigreeFile.png?raw=true "Pedigree file example")



# Parameter File

This is a simple keyword file with options and file names. 

![Screenshot of Parameter File](/Screenshots/ParameterFile.png?raw=true "Parameter file example")

These are the main ones. There are many more options in the documentation. 

# Output Files

* genotypes_imp.txt
* org_vs_imp.txt
* parentage_test.txt
* ref_pop.txt
* report.txt
* snp_info.txt
* stat_anim_imp.txt
* stat_anim.txt
* stat_snp_imp.txt
* stat_snp.txt

genotypes_imp.txt

![](/Screenshots/genotypes_imp.png)

org_vs_imp.txt

![](/Screenshots/orig_vs_imp.png)

parentage_test.txt

![](/Screenshots/parentage_test.png)

ref_pop.txt

![](/Screenshots/ref_pop.png)

report.txt

![](/Screenshots/report.png)

snp_info.txt

![](/Screenshots/snp_info.png)

stat_anim_imp.txt

![](/Screenshots/stat_anim_imp.png)

stat_anim.txt

![](/Screenshots/stat_anim.png)

stat_snp_imp.txt

![](/Screenshots/stat_snp_imp.png)

stat_snp.txt

![](/Screenshots/stat_snp.png)




