# Polygenic-Adaptation-score
 Trait score (TS)-based method used in Guo et al.[1] which was originally proposed by Robinson et al. [2] to estimate the deviation of the TS of a population from the overall mean. We calculated the TS for each individual as g=∑Ll=1βlxl, where x represents the count of alleles with respect to the effect size of each SNP (0, 1, or 2).

1.	Guo J, Wu Y, Zhu Z, Zheng Z, Trzaskowski M, Zeng J, et al. Global genetic differentiation of complex traits shaped by natural selection in humans. Nat Commun. 2018;9:1865.
2.	Robinson MR, Hemani G, Medina-Gomez C, Mezzavilla M, Esko T, Shakhbazov K, et al. Population genetic differentiation of height and body mass index across Europe. Nat Genet Vol. 2015;47:34.
#################################################################################################################################
First, you'll need to run a GWAS using PLINK and obtain the results in a file format that can be easily read and processed in R, such as a .bed, .bim, and .fam file.
Next, you'll need to load the PLINK GWAS results into R using the plink() function from the "plink" library.
	After that, you can extract the necessary information from the GWAS results, such as the effect size (beta) and allele count (x) for each SNP. This can be done using the extract() function from the "plink" library.
Now you can define the formula g=∑Ll=1βlxl, where x represents the count of alleles with respect to the effect size of each SNP (0, 1, or 2).
Then, you can create a loop that iterates over all SNPs, summing up the product of beta and x for each SNP.
Finally, you can save the result of the calculation as the polygenic adaptation score
