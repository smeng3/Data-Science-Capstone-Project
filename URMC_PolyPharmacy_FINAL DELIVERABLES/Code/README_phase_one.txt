FILE NAME: Phase_One.ipynb 
========


# Phase One 

Phase One of this capstone project is a data cleaning script for dealing with misspelling words matching.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install all the package and environment.

```bash
pip3 install Python3
pip3 install jupyter
pip3 install pandas
pip3 install numpy
pip3 install csv
pip3 install difflib

```

# Usage 

## SEC.0: LOAD PACKAGES
 #### Run the 1st cell to load package

## SEC.1: Read input Data

#### Edit and run the 1st cell 
	Change or update the relative path to the target file at 1st variable named "path_to_input_target"
	Change or update the drug name column in the csv file at 2nd variable named "target_drug_column"
	Change or update the patient id column in the csv file at 3rd variable named "target_patient_column"

	Change or update the relative path to the library file at 4th variable named "path_to_input_lib"
	Change or update the drug name column in the csv file at 5th variable named "lib_drug_column"
	Change or update the generic name column in the csv file at 6th variable named "lib_drug_generic"
	Change or update the generic name separator (Ex.two generic name in one row, separate by "/") in the csv file at 7th variable named "lib_separator"

#### Run the 2nd and 3rd cell to read in and re-formatting csv files.

## SEC.2: Clean data by generic name matching

#### Run 1st cell to create 1 function ("check_generic_name")
This function handles matchings and calculations of the alphabet frequency patterns ratio on each combination of words in generic names.

#### Edit and run the 2nd cell
	Change the 1st variable named "THRESHOLD" for matching cutoff ratio which is a float in the range (0, 1]. 

#### Run 3rd cell to get a summary report of generic matching result
* "**Directly matching**" : total number of words exact matched in the generic name list

* "**Algorithm correction**" : total number of words matched by alphabet frequency patterns under the "**THRESHOLD**" (cutoff ratio) above.

* "**Unknown value**": total number of words not matched in this section.

## SEC.3: Clean data by trade name matching
 
#### Run 1st cell to create a function ("check_trade_name")
This function handles matchings and calculations of the alphabet frequency patterns ratio on each combination of words in trade names.
 
#### Edit and run the 2nd cell
	Change the 1st variable named "THRESHOLD" for matching cutoff ratio which is a float in the range (0, 1]. 

#### Run 3rd cell to get a summary report of generic matching result
* "**Total Correction Number**" : total number of words corrected or matching in this whole process.
* "**Directly matching**" : total number of words exact matched in the trade name list.
* "**Algorithm correction**" : total number of words matched by alphabet frequency patterns under the "**THRESHOLD**"(cutoff ratio) above.
* "**Unknown value**": total number of words not matched in SEC.2 and SEC.3.
* "**Warning**" : total number of words having different first alphabet letter to the algorithm correction output words.

## SEC.4: Path to output file
#### Edit and run the 1st cell
	Input a path of an csv output file in the 1st variable named "path_to_output"
	 