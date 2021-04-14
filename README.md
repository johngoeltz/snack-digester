# snack-digester

Readme file for Snack Digester
Last updated Feb 21, 2021 by John Goeltz, johngoeltz at gmail dot com


I wrote the Snack Digester as a way to introduce young scientists (e.g., first year college students) to automated text processing in the context of chemistry.
It is written in Python 3.0 and was developed in Google Colab but also works in Jupyter and similar environments.

The user types or pastes the ingredients from a highly processed food or household product (e.g., barbeque potato chips or hair conditioner).
The code cleans up any punctuation it may find before splitting the ingredients text string into a list of individual ingredients.
The code then uses a Python package called CIRpy to "resolve" each ingredient using the PubChem servers at the National Institutes of Health (NIH).
Essentially, the NIH servers scan their huge list of known substances and compounds to see if each set of words in the list of ingredients is a known chemical.
If the item is a name or nickname for a chemical (e.g., salt), NIH returns a SMILES string, a machine-readable notation for chemical structure.
If the item is not a chemical (e.g., milk), NIH returns "None".
The code then uses the pandas package to organize and clean up the results, dropping duplicates and "None" values.
A csv file is the output.  This file can be used in other cheminformatics software such as DataWarrior, or groups of results can be aggregated and analyzed.

