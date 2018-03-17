# silva-survey.py
Program for inferring isolation source from a clade of organisms in SILVA

The latest release of the SILVA database of candidate small-subunit (SSU) 16S rRNA gene sequences encompasses over 6 million sequences. These sequences are derived from a variety of sources, including isolated cultures, as well as those derived from environmentally-derived sources. This database, thus, represents a useful repository for assesing the diversity and environemtal distribution of microbial life on Earth.

The silva-survey program takes as input any taxanomically-derived name that would be found in a SILVA sequence header. This name could be at any taxanomic level, as specific as "Shewanella" and as broad as "Bacteria". The second required input is the SILVA database, which can be downloaded from https://www.arb-silva.de/no_cache/download/archive/current/Exports/. The file you want is "SILVA_132_SSUParc_tax_silva.fasta.gz". In the next release, the 132 in SILVA_132_SSU... will be replaced with 133.


With the SILVA database and any taxanomic name as input, the program will output a csv file for each SILVA entry that matched the inputted name: output will include the sequence header, isolation source, literature reference for the sequence, and the RNA nucleotide sequence of the gene.

SAMPLE USAGE:

    python3 silva-survey.py -taxa Zetaproteobacteria -silva_DB /Path/to/SILVA/SILVA_132_SSUParc_tax_silva.fasta -out_dir /Path/to/output/


The only dependency for this program is python3
