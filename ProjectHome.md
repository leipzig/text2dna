# Rationale #
The goal of this project is to provide a set of scripts to convert text or written words into a series of DNA nucleotides.

My purpose is to use this to visualize genomic assembly algorithms in an intuitive, readable manner.

# Downloading #
Type the following on your command line to obtain the two scripts (text2dna.pl and dna2text.pl):
```
svn checkout http://text2dna.googlecode.com/svn/trunk/ text2dna-read-only
```

# Usage #
## Encoding ##
The description above was saved to description.txt
```
:>perl text2dna.pl < description.txt > description.fa

:>cat description.fa
>Seq_1
GGGAGCCAGCGGGCGTGCTTGCAGGCTAGCTTGCGCGTGAGCCAGCCGGTATGTAAGTACGCTTGCCCGCGGGCATGTGAGCCGGTATGTGAGCTTGTAAGTACGCTTGTGCGCCGGCGAGCGGGCAGGTATGCGGGTGAGCTTGCGCGTATGCATGTACGCCGGTAAGTGAGTATGTGAGCTTGCATGCTTGCTCGTGCGCGGGTACGTGAGTGAGCGGGTCAGTGAGCTTGTACGTGTGTACGCCGGTGAGTGAGCGGGCTCGTGTGCTTGTACGCGAGTATGCCGGCTCGTGAGCTTGCAGGTATGCGGGTACGCCGGCGGGTATGCTTGCGCGAGAGATCGAAGGCTCGTGGGCATGCTAGCGGGCTTGTGAGCCGGCGAGCGGGTATACTC
>Seq_2
GATGGTCGGTAAGTGGGTACGTAAGCTTGTATGCGGGCCGGTATGTGAGCTTGTGGGTATGCGGGTGAGCCAGCCGGTATGTGAGCTTGTGCGCCGGTATGTGGGCAGGCTAGCCGGTCCGCGGGCGTGCGGGCTCGCTTGCTGGCCGGCATGCAGGTATGTATGCGGGCTGGCACGCTAGTCGGCAGGCTAGCGTGCTTGTACGCCGGTGAGCCAGCTGGTATGCCGGCTCGCAGGCTCGCCGGCTCGTGAGTGGGCCGGTGAGCCGGTGCGCGGACTAGTACGCGGGCAGGCGAGCAGGCACGCTAGCGGGCTGGCAGGCTCGCTCGCGGGTACACTC
```

## Decoding ##
```
>perl dna2text.pl < description.fa
>Seq_1
ThegoalofthisprojectistoprovideasetofscriptstoconverttextorwrittenwordsintoaseriesofDNAnucleotides.
>Seq_2
Mypurposeistousethistovisualizegenomicassemblyalgorithmsinanintuitive,readablemanner.
```

Notice the spaces are missing - this is my own personal preference as the assemblers I work with cannot handle the number of spaces English introduces. You can comment the `s/\s//g` if you wish to preserve spaces.