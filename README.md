# getHorizonsData
 A Code for Pulling Data from JPL Horizons

There are two functions you can use in this python code.

makeHorFile(objectName): 
 This function accepts a string of an object's name or ID, and outputs a csv file in the same file/repo
 as the code.
 In reality, This function will technically currently output 2 csv files, one with a column for geocentric julian datetime, and one for the 
 KBO centric julian datetime. Aside from that, both files will also have equivalent RA and DEC columns for the date specified.
 The data spans a time period of 70 years, from 01-01-1950, to 01-28-2020, with a step size of 1 day. On my personal laptop, the runtime 
 for this function is around 170 seconds, so it should be much faster on any other computer.
 
geoToKBOTime(fileName):
 This function accepts an object name, which has a geocentric csv file in the same directory, and converts that CSV's data into KBO centric 
 time. All of the parameter's are readin I input them into my BenecchiData_geoTime.csv file, which may not be how those types of files are 
 typically formatted largely, so that formatting options of the dataframes can be changed quite easily to accomodate that. This function 
 will just read in the list of dates that were previously used, and will just use them again. These must be julian dates.
