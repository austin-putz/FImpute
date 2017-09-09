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

