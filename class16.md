# Intro to UNIX
Diego Diaz, PID: A17328629

## Basic Unix

Some important file system commands include:

pwd : print working directory ls : list files and folders cd : change
directory mkdir : make a new directory rm : delete files and directories
nano: a very basic text editor that is always available  
less: to view/read text files page by page (page viewer)

My AWS instance:

ssh -i “BIMM143DiegoDKey.pem”
ubuntu@ec2-34-219-59-96.us-west-2.compute.amazonaws.com

To copy from my AWS instance:

scp -i ~/Desktop/BIMM143/BIMM143DiegoDKey.pem
ubuntu@ec2-34-219-59-96.us-west-2.compute.amazonaws.com:~/work/results.tsv
.

> Q. What does the star character accomplish here? Ask Barry, or your
> class neighbor, if you are not sure!

The star is like a wildcard character, acts a shortcut to enter instead
of a directory’s name.

> Q. How many sequences are in this mouse.1.protein.faa file? Hint: Try
> using grep to figure this out…

55052 sequences

> Q. What happens if you run the above command without the \>
> mm-first.fa part?

A new file containing the head of the first mouse file will not be
generated. since it has no output file name.

> Q. What happens if you were to use two ‘\>’ symbols (i.e. \>\>
> mm-first.fa)?

This will also not create a file as this command wants to input the head
information into an existing file.

Reading zebrafish results.

``` r
zfres <- read.delim("results.tsv", header = FALSE)
colnames(zfres) <- c("qseqid", "sseqid", "pident", "length", "mismatch", "gapopen", "qstart", "qend", "sstart", "send", "evalue", "bitscore")
```

Making a histogram with R of bitscores.

``` r
hist(zfres$bitscore,
     breaks = 30,
     main = "BLAST Bitscores",
     xlab = "Bitscore")
```

![](class16_files/figure-commonmark/unnamed-chunk-2-1.png)

``` r
plot(zfres$pident * (zfres$qend - zfres$qstart),
     zfres$bitscore,
     xlab = "Percent Identity × Alignment Length",
     ylab = "Bitscore",
     main = "Relationship Between Identity and Bitscore")
```

![](class16_files/figure-commonmark/unnamed-chunk-3-1.png)

> Q. Note the addition of the -r option here: What is it’s purpose? Also
> what about the \*, what is it’s purpose here?

The -r will copy directories instead of individual files. The \* will is
so that every file in the “work” directory is copied.
