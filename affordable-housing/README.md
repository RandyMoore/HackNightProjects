# affordable-housing-sanjose
A python converter to visualize affordable housing data for San Jose on an html page.
It optionally allows for generation of a kml file.

# Dev Setup #

Python
Eclipse For Python

# Dependencies #

Install the usaddress python library to parse address strings - pip install usaddress

usaddress(https://pypi.python.org/pypi/usaddress)

# Resources #

San Jose affordable-housing datasets - 
The steps to download the dataset to use are 
1 - Access http://data.sanjoseca.gov/datasets/165367/affordable-housing-data/
2 - Select any affordable housing data set of your choice
3 - Select Export to CSV option on the left panel by clicking on the download icon.

Code Enforcer link - http://www3.sanjoseca.gov/codeEnforcement/cets/form_index.asp

# How to generate a html output#
python CSVToHTMLTemplate.py <housing dataset csv> <name of the html output file> 

Example :
python CSVToHTMLTemplate.py PublishAffordableExcelCSV.csv housing.html

The resulting html file will contain an html table with the property listings.

# How to generate a kml output#
python CSVToKML.py <housing dataset csv> <name of kml output file>

Example :
python CSVToKML.py PublishAffordableExcelCSV.csv housing.kml

The resulting kml file will contain placemarks that display property information. 

#Open issues#

All the addresses do not conform to the US address conventions. Their format differs so we are unable to identify the Street Direction accurately.

Cannot access the code enforcer url via javascript because of CORS issues.

CURL posts to the code enforcer url work fine.







