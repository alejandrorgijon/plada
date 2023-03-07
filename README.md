# plada

The package `plada` aims to help you <i><b>PLA</b>ying with your <b>DA</b>ta</i> (quite original name, huh?). 

## Installation

This package is currently only available through GitHub and can be downloaded using devtools.

```
> install.packages("devtools")
> devtools::install_github("alejandrorgijon/plada")
```
## Functions

At the moment, `plada` has 5 functions that have been quite useful to manage and sort data. 
The package also includes 2 fake datasets (`sequences` and `random_data`) to test the functions included here.

### `gesize()`: 
This function calculates the GC percentage of given sequences and calculates the length of them (aka number of bases).
For example, I have provided in the package a fake dataset of genetic sequences called `sequeneces`:

```
> head(sequences)
1       seq1    GCGCGCGGGCATCGTAGCTGCTCGCGCTAGCTACGTCCGCTCTCGACTAGCTGACTGCGCTCAGCTATGCTACGATCGTACGATCGTGCTATGCTAGTGCATGCTAGCTAGC
2       seq2    CGATCGTAGCTACGTAGCTAGCTGATCGACTAGTGATCGCGTAGCTAGCTGCTGCTCGTCGTATGACTAGCTGATCGATCGATCGATCGTAGCTAGCTAGCTAGCTGATCGTAG
3       seq3    cgatcgcgatcgtactgctgtcggtggcta
4       seq4    cgatactcatatgcgtcgtaacgtctgctgtgtgtgctactatcgtagctacgtacgatcgatcgtgactcgatcgtagactg
5       seq5    ACTCGTAGCGTTGGTCATcatcgtagctagcgctagctgatgccaaaaa
```

If we use the function `gesize(), indicating which column has the genetic sequences and which column has the name given to the sequence, we can retrieve the GC composition and length of the sequence:

```
> gesize(sequences$genseqs, sequences$columnames)
name    length    GC        sequence
1 seq1   112      59.82    GCGCGCGGGCATCGTAGCTGCTCGCGCTAGCTACGTCCGCTCTCGACTAGCTGACTGCGCTCAGCTATGCTACGATCGTACGATCGTGCTATGCTAGTGCATGCTAGCTAGC
2 seq2   114      51.75    CGATCGTAGCTACGTAGCTAGCTGATCGACTAGTGATCGCGTAGCTAGCTGCTGCTCGTCGTATGACTAGCTGATCGATCGATCGATCGTAGCTAGCTAGCTAGCTGATCGTAG
3 seq3   30       60       cgatcgcgatcgtactgctgtcggtggcta
4 seq4   83       49.4     cgatactcatatgcgtcgtaacgtctgctgtgtgtgctactatcgtagctacgtacgatcgatcgtgactcgatcgtagactg   
5 seq5   49       48.98    ACTCGTAGCGTTGGTCATcatcgtagctagcgctagctgatgccaaaaa 
```
                                                                                                           
### `meancat()`: 
Calculates the mean of a numerical variable (n) according to certain category (m) –> meancat(n, m).

```
head(random_data)

### `percencat()`: 

### `taxabu()`: 

### `which_envi()`: 

