### PGxInsight ###
PGxInsight software was developed as part of the Hudson Alpha Tech Challenge 2022 in efforts to afford more comprehensive Pharmacogenomic services to providers which integrate multiple Pharmacogenomic databases & allow easy query of genetic test results. Please see https://hudsonalpha.org/techchallenge/ for more information on this challenge. 

##METHODS##
1. CPIC sql databases were parsed in pgAdmin 4 with postgresql. A csv file of each CPIC table was exported from pgAdmin4. The CPIC csv files & PharmGKB tsv files were converted to tab delimited text utilizing sed 's/,/\t/g' in bash. An Rscript was then utilized to perform full joins on the database based on a column with a common field.
2. The Sample_Genetic_Data.json was parsed in Excel and converted to tad delimited text. 
3. The Sample_Genetic_Data.txt file was utilized to search gene variants in the integrated CPIC & PharmGKB database from the command line which generated the PharmGenResults1.txt report.
4. An user-interface was created to allow providers the ease of uploading thier genomic data reports which are then searched against an integrated PharmGKB and CPIC database to generate a pdf report tailored to a physician's preference.

##App##
http://share.streamlit.io/kostrouc/HATCH2022/master/streamlit_app.py

Citation:

Casey, D., Carter, J., Ostrouchov, K. (2022). PGxInsight. github.org. Available from: https://github.com/kostrouc/HATCH2022/ 

