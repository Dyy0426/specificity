Specificity Package Documentation
Overview
The specificity package is designed to calculate the specificity of barcode sequences against a set of species sequences. It provides tools for reading sequences from a file, calculating the average nucleotide specificity, and exporting the results to an Excel file.

Installation
To install the specificity package, run the following command:
pip install specificity

Usage
The specificity package contains several functions that can be used to process sequence data and calculate specificities.

1.Reading Sequences from Files
To read sequences from a file, you can use the read_sequences_from_file function:

from specificity import read_sequences_from_file

file_path = 'path_to_your_file.txt'
sequences = read_sequences_from_file(file_path)
This function takes a file path as input and returns a list of sequences, excluding any lines starting with > and replacing - with N.

2.Calculating Specificity
To calculate the specificity of a barcode sequence against a set of species sequences, use the calculate_specificity function:

from specificity import calculate_specificity

barcode_sequence = 'ACTG...'
species_sequences = ['ACTG...', 'ACGG...', ...]
average_nucleotide_specificity, average_specificity_cases = calculate_specificity(barcode_sequence, species_sequences)
It returns the average nucleotide specificity and a dictionary with average specificities for different numbers of nucleotide differences.

3.Processing Files and Exporting Results
The process_files function combines reading sequences and calculating specificities to process multiple files and export the 

results:

    from specificity import process_files

    barcode_file_path = 'path_to_your_barcode_file.txt'
    species_folder_path = 'path_to_your_species_sequences_folder'
    output_excel_path = 'path_to_output_excel_file.xlsx'

process_files(barcode_file_path, species_folder_path, output_excel_path)
This function reads barcode sequences from the given file, calculates their specificities against species sequences found in the specified folder, and outputs the results to an Excel file.

Contributing
Contributions to the specificity package are welcome. Please consider the following ways to contribute:

Reporting bugs
Suggesting enhancements
Sending pull requests for bug fixes or feature additions
For more details on contributing, please refer to the CONTRIBUTING.md file (if available).

License
The specificity package is released under the MIT License. Please refer to the LICENSE file for more details.
