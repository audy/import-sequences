# Run Illumina

Demultiplex Illumina 16S rRNA data from multiple formats into a single,
consistent format.

This way, downstream pipelines can make dumb assumptions about data format.

(c) 2014, Austin G. Davis-Richardson

## TODO

### Supported Input Types:

- FASTQ
  - paired, barcoded
  - paired
- QSEQ
  - paired, barcoded
  - paired

### Example Output

Output will always be in interleaved FASTQ format with or without the barcode
sequences at the end of the header.

#### FASTQ (paired, barcoded)


```
@HWUSI-EAS163FR:7:4:107:1355:1011:0:1:NNNNNNN
NNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNNN
+HWUSI-EAS163FR:7:4:107:1355:1011:0:1:NNNNNNN
BBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBB
```

Barcode sequence will be at end, pairs are *interleaved*.

#### FASTQ (paired)

```
@HWI-6X:10323:5:101:995:948:0:1
NCTCAGCTGCCACATCCAATTATGCTCTCCAGGCCATGTGTTGGGGGCTATCTCCTTAATCAACTGACTGCTTTAATGGTAGGCAACCCCAGCACCGTCCC
+HWI-6X:10323:5:101:995:948:0:1
BBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBB
@HWI-6X:10323:5:101:995:948:0:2
ACTGTTTTGAAACCTCAGAAGTGAGGCAGTGTAGCATTCAAGGGTAAAGCAGCATGCTGGAGGAACGTGCGGAGAAGTTCAGGGGAGGCTTTTCTTCCTTG
+HWI-6X:10323:5:101:995:948:0:2
```

No sequence, pairs are *interleaved*.
