# Election_Analysis 

## Overview of Election Audit
The Election Commission has hired the Colorado Board of Elections to perform an audit on election results for a congressional precinct in Colorado. The goal of this project is to develop an automated process for auditing election results using Python so that it can be applied to other government election audits. 

## Resources
- Data Source: election_results.csv
- Software: Python 3.7.6, Visual Code Studio, 1.54.1

## Election-Audit Method
In order to perform the election audit, Python script was written as shown in the images below to yield the total votes, votes per county, county with the largest turnout, votes per candidate and the winning candidate results. 

### Dependencies, Variables, Lists and Dictionaries
- The csv module was imported to read and write the data in the csv format and os module was imported to use indirect paths for opening the required files.
- Variables were initialized for the total votes, winning candidate data and largest county data.
- A list was created for the candidate options and counties. 
- A dictionary was created where the value was the vote count and the keys were the candidate and counties.

![Py_Poll_Code1](https://user-images.githubusercontent.com/78664640/111921530-7a204100-8a6b-11eb-9706-8a33164e2b61.png)

### Reading and Extracting the Election Results
- A with statement was used to open the election results file to be read. 
- A for loop was used to iterate through the rows in the election data csv file in order to extract the total vote count, candidate name and county names.  
- An if statement with a not in membership was used inside the for loop to get the unique candidate names and county names. 

![Py_Poll_Code2](https://user-images.githubusercontent.com/78664640/111921541-84dad600-8a6b-11eb-8a19-7337eebbdcc1.png)

### Saving the Election Results to the Analysis File
- A with statement was used to open the election analysis text file so that we can write the data to it. 
- A for loop was used to loop through the counties to retrieve the vote count and percentage per county. An if statement was used to determine the largest county voter turnout. The results were then printed and written to the analysis file.  
- A for loop was used to loop through the candidates to retrieve the vote count and percentage per candidate. An if statement was used to determine the winning candidate and their respective votes and percentage. The results were then printed and written to the analysis file. 

![Py_Poll_Code3](https://user-images.githubusercontent.com/78664640/111922382-d84f2300-8a6f-11eb-8b0f-1a7fbe79c852.png)
![Py_Poll_Code4](https://user-images.githubusercontent.com/78664640/111921547-8dcba780-8a6b-11eb-9faf-9a1fc168da56.png)


## Election-Audit Results
- Total Votes: 369,711

- Votes per County:
  - Jefferson: 10.5% (38,855)
  - Denver: 82.8% (306,055)
  - Arapahoe: 6.7% (24,801)

- Largest County Turnout: Denver

- Votes per Candidate
  - Charles Casper Stockham: 23.0% (85,213)
  - Diana DeGette: 73.8% (272,892)
  - Raymon Anthony Doane: 3.1% (11,606)

- Winning Candidate Results
  - Winner: Diana DeGette
  - Winning Vote Count: 272,892
  - Winning Percentage: 73.8%

## Election-Audit Summary
The project shows that using Python code to audit the election results was successful. The Colorado Board of Election is proposing that the Election Commission apply the same audit method using Python script to other elections to automate the process. The following examples show how the Python code can be modified to apply the same methodology to all the congressional precincts in Colorado:
- A new list can be created to include all the precincts in Colorado and a dictionary where the precinct is the key and the vote count for each precinct is the value. 
- The for loop can be modified to add another loop to iterate through the precincts election data. 
