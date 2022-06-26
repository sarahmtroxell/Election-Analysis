# Election-Analysis

## Project Overview
A fictional Colorado Board of Elections employee has asked for help auditing results of a congressional election. The election commission has asked them for the following data: 

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who recieved votes.
3. Calculate the total number of votes and percenatge of votes each candidate recieved.
5. Determine the winner of the election based on popular vote.
6. Calculate the total number of votes and percenatge of votes each cast in each county.
7. Determine which county had the largest voter turnout.

## Resources
The Colorado Board of Elections provided complete data from the recent election in a CSV file. My approach was to use Python and Visual Studio Code to write a script that read the election data, calculated the required statistics, then created a TXT file with the output to easily share my results.
- Data Source: election_results.csv
- Software: Python 3.9.12, Visual Studio Code, 1.67.2
- Output File: election-analysis.txt

    ```
    Election Results
    -------------------------
    Total Votes: 369,711
    -------------------------

    County Votes:
    Jefferson: 10.5% (38,855)
    Denver: 82.8% (306,055)
    Arapahoe: 6.7% (24,801)

    -------------------------
    Largest County Turnout: Denver
    -------------------------
    Charles Casper Stockham: 23.0% (85,213)
    Diana DeGette: 73.8% (272,892)
    Raymon Anthony Doane: 3.1% (11,606)
    -------------------------
    Winner: Diana DeGette
    Winning Vote Count: 272,892
    Winning Percentage: 73.8%
    -------------------------
    ```

## Results
The analysis of the election by county show that: 
- There were 369,711 votes cast in the election.
- The county results were: 
  - 82.8% of votes or 306,055 total votes were cast in Denver county.
  - 10.5% of votes or 38,855 total votes were cast in Jefferson county.
  - 6.7% of votes or 24,801 total votes were cast in Arapahoe county.
- Denver county had the largest number of votes, where 306,055 votes were cast.
- The cadidate results were: 
  - Charles Casper Stockham recieved 23.0% of the vote and 85,213 number of votes.
  - Diana DeGette recieved 73.8% of the vote and 272,892 number of votes.
  - Raymon Anthony Doane recieved 3.1% of the vote and 11,606 number of votes.
- The winner of the election was: 
  - Diana DeGette, who recieved 73.8% of the vote and 272,892 number of votes.

## Summary
The output of this script contains accurate statstical data that can be used to determine the winner of any election along with voter turnout data by county. If the results file format is changed, your team can easily fix the code to continue to work. Additonally, this script may be easily used by your team to audit future elections, whether they are at the local level or have a larger data set, such as the state level. The script may also be modified to extract and summarize additonal data about voters and the votes recieved.

### Election Results File Format
This code was built to function properly using the "election_results.csv" input file provided by your team. This file contained the Ballot ID, County, and Candidate Name chosen by columns in order. The code was written to function properly with input files where the second column must include the County the vote was cast in and the third column must contain the full name of the candidate voted for. If future election files have the County or Candidate Name data in a different column location, you will have to modify the code where that index is referenced. The picture below shows the two lines of code that would need to be updated if the column order changed. 

```
# Get the candidate name from each row.
candidate_name = row[2]
# Extract the county name from each row.
county_name = row[1]
```

Please note that Python indexing begins at zero, so even though the Candiaate Name is in the third column of the input file, the code needs to reference the second index. If the Candidate Name moved to the sixth column of data and the County moved to the first column in a future output file, the code will need to be modified as shown below. 

```
# Get the candidate name from each row.
candidate_name = row[5]
# Extract the county name from each row.
county_name = row[0]
```

### Demographic Information
The Board of Elections may want to know demographic information about the citizens that voted in a future election. This code can easily be modified to include data such as the percent of voters by gender, age, or income. This data would need to first be collected and inserted into the election_results.csv file. Then, 


