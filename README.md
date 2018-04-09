# silva-survey.py
Program for inferring environmental distribution based on isolation sources from clades of organisms in SILVA.

The latest release of the SILVA database of candidate small-subunit (SSU) 16S rRNA gene sequences encompasses over 6 million sequences. These sequences are derived from a variety of sources, including isolated cultures, as well as those derived from environmentally-derived sources. This database, thus, represents a relatively useful repository for assesing the diversity and environmental distribution of microbial life in the environment.

The silva-survey program takes as input any taxanomically-derived name that would be found in a SILVA sequence header. This name could be at any taxanomic level, as specific as "Shewanella oneidensis" and as broad as "Bacteria". The second required input is the SILVA database, which can be downloaded from https://www.arb-silva.de/no_cache/download/archive/current/Exports/. The file you want is "SILVA_132_SSUParc_tax_silva.fasta.gz". As of April 2018, this is the latest release. In the next release, the 132 in SILVA_132_SSU... will be replaced with 133.


With the SILVA database and any taxanomic name as input, the program will output a csv file for each SILVA entry that matched the inputted name: output will include the sequence header, isolation source (if available), literature reference for the sequence, and the RNA nucleotide sequence of the gene.

SAMPLE USAGE:

    python3 silva-survey.py -taxa Zetaproteobacteria -silva_DB /Path/to/SILVA/SILVA_132_SSUParc_tax_silva.fasta -out_dir /Path/to/output/


The only dependency for this program is python3
