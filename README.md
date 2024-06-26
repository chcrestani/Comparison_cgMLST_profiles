This script takes in a table of cgMLST (or MLST) allelic profiles with each column representing an isolate and each row representing a locus('profiles.csv', no index column). The script is conceived to be launched on Jupyter Notebook.

The script is built to compare the profile of a reference isolate (column 'isolate_name') with that of other isolates whose name starts with the same prefix ('isolate_name_XXXXXXX').
In the original work, it was used to compare a reference short-read assembly (Illumina) with various long-read assemblies (generated e.g., with different depths of coverage, or basecalling algorithms)

Please note you should substitute 'isolate_name' with the name of the Illumina assembly and 'profiles.csv' with the name of your dataframe containing the alleleic profiles before running the script.

Missing loci in the Illumina assembly are masked and therefore are not included in the comparison. The results are stored as total number of mismatches in a dataframe ('df_isolate_name')
