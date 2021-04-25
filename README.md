# indico-json-to-latex
Python scripts to go form Indico's JSON format to latex formatting for an abstract booklet.

## Dependencies
The python libraries to be installed, e.g. via `pip install ...`
- sys
- json
- csv
- pandas
- time
- jupyter notebook

## Usage
### Export the JSON file from Indico:
1. Go into management mode on your indico site
2. Click on "Call for Abstracts" on the left column under organization
3. On "List of Abstracts" click "Manage"
4. Check all the abstracts
5. Under "Export" click "JSON"
6. This should download the file "abstracts.json" which contains all the information you need. 

### Creating your Conference Schedule
1. Create your conference schedule in excel (you can use whatever you want, but the weirder your format, the less plug-and-play this code will be).
   - For an example, ask for the .xlsx file from [WNPPC 2021](https://wnppc.triumf.ca/2021/).  

### Using the notebook
1. Open the jupyter notebook by writing `jupyter notebook` in the terminal once in the directory where this git repository is cloned. 
2. Change cell 2 line 10 of the notebook to be the filename (including location of the file) of your "abstracts.json" file you exported from indico earleir. 
3. Change cell 3 line 7 of the notebook to be the filename of your conference schedule .xlsx file
4. Run the notebook by going to the navigation bar and selecting "Kernel" -> "Restart and Run All"
5. Your latex file should now be in your current working directory and called "abstracts.tex"

## Future work and Development
This was a rough way of converting the abstracts into a latex booklet for WNPPC 2021. Some development can be done to make this script better. 

### To do:

1. Accept not-so-well formatted schedule files (e.g. accept csv, xls, txt, ... ) formats
2. Check the abstract ID variable that is pulled from the JSON is the public-facing ID that indico will have on the site for that abstract, and not some internal one. 
3. Also output a timetable in LaTeX based off the formatting desired. To do this, you just need to have a template and populate the variables in like how the abstract booklet was made. 

### Development and Contributing
If you do use this script, and/or develop it further, please do consider reaching out to me so you can commit your changes here and we can make future conference organisers lives easier. 


## Contact
If you have any questions, or would like to commit your code to this repository, feel free to reach out to me (soud.alkharusi _at_ mail.mcgill.ca)
