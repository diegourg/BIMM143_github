# Class 12
Diego Diaz, PID A17328629

- [Identify Genetic Variants of
  Interest](#identify-genetic-variants-of-interest)
- [Section 2: Initial RNA-Seq
  analysis:](#section-2-initial-rna-seq-analysis)

## Identify Genetic Variants of Interest

There are a number of gene variants associated with childhood asthma. A
study from Verlaan et al. (2009) shows that 4 candidate SNPs demonstrate
significant evidence for association. You want to find out what they are
by visiting OMIM <http://www.omim.org> and locating the Verlaan et
al. paper description.

> Q1: What are those 4 candidate SNPS?

The four candidate SNPS are rs12936231, rs8067378, rs9303277, and
rs7216389.

> Q2: What three genes do these variants overlap or effect?

These variants overlap/effect the genes ZPBP2, GSDMB, and ORMDL3.

Now, you want to know the location of SNPs and genes in the genome. You
can find the coordinates for the SNP itself on the Ensemble page along
with overlapping genes or whether it is intergenic (i.e. between genes).

> Q3: What is the location of rs8067378 and what are the different
> alleles for rs8067378?

rs8067378 is located at Chromosome 17: 39895095 (forward strand), the
different alleles are A/G variants (43% G.)

> Q4: Name at least 3 downstream genes for rs8067378.

ZPBP3, GSDMB, and ORMDL3 are downstream of rs8067378.

> Q5: What proportion of the Mexican ancestry in the Los Angeles sample
> population (MXL) are homozygous for the asthma associated SNP (G\|G)?

14% of the MXL sample population is homozygous for this asthma
associated SNP.

> Q6: Back on the ENSEMBLE page, use the “search for a sample” field
> above to find the particular sample HG00109. This is a male from the
> GBR population group. What is the genotype for this sample?

The genotype for this sample is G\|G.

## Section 2: Initial RNA-Seq analysis:

Using Galazy for NGS analyses.

> Q7: How many sequences are there in the first file? What is the file
> size and format of the data?

There are 3863 sequences in the first file. This a 741.2kb fastqsanger
file.

> Q8: What is the GC content and sequence length of the second fastq
> file?

The GC content of the second file is 54%. The sequence length is 50-75.

> Q9: How about per base sequence quality? Does any base have a mean
> quality score below 20?

The is no base where the per base sequence quality score is less than
20.

> Q10: Where are most the accepted hits located?

Most of the hits are around 38,150,000bp.

> Q11: Following Q10, is there any interesting gene around that area?

PSMD3.

> Q12: Cufflinks again produces multiple output files that you can
> inspect from your right-handside galaxy history. From the “gene
> expression” output, what is the FPKM for the ORMDL3 gene? What are the
> other genes with above zero FPKM values?

The fpkm for ORMDL3 is 136853. Other genes with non-zero fpkms are
PSMD3, GSPMA, GSPMB, and ZPBP2.
