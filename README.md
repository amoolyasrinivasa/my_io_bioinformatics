# my_io.py
This is a python module that contains the function get_fh() which is used in all the three programs below. Anytime a file needs to be opened for reading or writing in your programs in this assignment, the program calls on this module's function get_fh() function. 
The other function in the module is is_valid_gene_file_name() that will check to make sure the given file name exists, if it does it returns True else it will return False.

# config.py
This python script is a small configuration module.
Instead of copying large files needed for the program, we can create a variable in config.py and set it to the directory. It can be done by assigning the path to a variable in the beginning of the script as shown below:

_UNIGENE_DIR = "/data/PROGRAMMING/assignment5"
_UNIGENE_FILE_ENDING = "unigene"
The function get_unigene_directory(), returns the variable _UNIGENE_DIR.
The function get_unigene_extension, returns the variable _UNIGENE_FILE_ENDING.
The function get_host_keywords, returns a dictionary of the hosts that will be found in assignment5.config.py module. This will be a dictionary for the mapping. This will be used map common names with scientific names. 

# Gene_information_query.py
This python program takes in two arguments - host name and gene name - and allows us to query the tissue data from the unigene directory of six mammals.

## Description
This program takes common names as well as scientific names for the host as shown below:

Homo_sapiens or Homo sapiens or Human or Humans
Bos_taurus or Bos taurus or Cow or Cows
Equus_caballus or Equus caballus or Horse or Horses
Mus_musculus or Mus musculus or Mouse or mice
Ovis_aries or Ovis aries or Sheep or Sheeps
Rattus_norvegicus or Rattus norvegicus or Rat or Rats

The gene option will take a gene name like 'PWRN1, ESF1, PVRL1 and this option will be used to see if the gene exists in the given host directory. If the gene does exist then it will be used for the data output. If not, tell the user it does not exist and exits the program.

## Getting started

## Dependencies
Runs on linux or any other CLI

## Installing
The programs can be found on the programming6200/assignment5 directory on defiance

## Executing programs
$ python3 gene_information_query.py
$ python3 gene_information_query.py -host horse -gene API5
$ python3 gene_information_query.py -host "Homo sapiens" -gene AATK
$ python3 gene_information_query.py -host Homo_sapiens -gene EXD1
