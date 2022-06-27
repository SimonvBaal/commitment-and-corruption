# commitment-and-corruption

This project contains a raw-data folder, the files in which are loaded by the 
cleaning*.Rmd files.
The cleaning files then deposit a new clean data file in the 'data' subfolder.

The analysis.Rmd files contain the data analysis and the figures.Rmd files 
contain the visualisation.
The figures subfolder will be used when the analysis file is run to store the 
plots generated by the markdown files.

The environment can be loaded by running load(".RData"), and the packages can be 
loaded by running "renv::restore()".

## Instructions
It is best to run both the cleaning files first, then run the analysis files and
finally the figures files.

To do this, download the entire project and click on the .Rproj file. Then,
open all the .Rmd files and run them one by one - the ordering matters.

If desired, one can look at the individual results by running commands such as
summmary(). 


-- 
## Codebook

There are *collaborative*.csv and *individual*.csv files in the raw-data subfolder. These are both part of the die rolling task, but the software spits out separate files.
They share a common language.

*collaborative*.csv files
group = the experimental session
subject = the participant within the session, important for the collaborative pairings. Odds are first movers, evens are second movers.
team = participants in the same team are playing with one another in the collaborative pairings.
stage = indicates whether participants are first or second movers.
condition = can be ignored. Should always be forced.
type = can be ignored.
response = the die roll report.
error1 = can be ignored.
comment = can be ignored.
RT = reaction time.

*individual*.csv files
label = indicates what response was being elicited: 
- roll1-5 are practice trials
- Q1-4 were checks to see whether participants understood instructions
- roll101-118 are pre collaboration trials
- roll201-218 are post collaboration trials

The names for the columns in the *exp2* files should make more sense knowing the above.



