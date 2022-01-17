# election-analysis
## Project Overview
A Colorado Board of Elections employee has given you the following tasks to complete the election audit of a recent local congressional election.
  1. Calculate the total number of votes cast. 
  2. Get a complete list of candidates who received votes.
  3. Calculate the total number of votes each candidate received.
  4. Calculate the percentage of votes each candidate won.
  5. Determine the winner of the election based on popular vote.

## Resources
  - Data Source: election_results.csv
  - Software: Python 3.6.1, Visual Studio Code, 1.38.1

## Summary
The analysis of the election shows that:
  - There were 369,711 votes cast in the election. 
  - The candidates were:
    - Charles Casper Stockham
    - Diana DeGette
    - Raymon Anthony Doane
  - The candidate results were:
    - Candidate Stockham received 23.0% of the vote and 85,213 votes total.
    - Candidate DeGette received 73.8% of the vote and 272,892 votes total.
    - Candidate Doane received 3.1% of the vote and 11,606 votes total. 
- The winner of the election was:
    - Diana DeGette, who received 73.8% of the vote and 272,892 votes total.

## Challenge Overview
### Challenge Purpose
- The purpose of this challenge was the add county-specific data to existing data on election results. 

### County-Specific Data
- Denver County had the largest turnout. 
  - Denver County made up 82.8% of the vote with 306,055 votes.
- Jefferson County had the second largest turnout.
  - Jefferson County made up 10.5% of the vote with 38,855 votes.
- Arapahoe County had the smallest turnout.
  - Arapahoe County made up 6.7% of the vote with 24,801 votes.

## Challenge Summary
This program could be an excellent resource for the Election Commission. Because the script is written with variables, pulling from a CSV, the code can be easily modified to fit any election data. 

For example, we could pull any election results into this script by adjusting the file path here: 

  Add a variable to load a file from a path.
  file_to_load = os.path.join("Resources", "election_results.csv")

Once the election results have been loaded, we would only need to make a few modifications to the code. For example, if the election commission wanted to add political party data, that would be a simple addition to the code. We could quickly and easily mimic the for loop here in order to add an analysis of political party data:

  For each row in the CSV file.
    for row in reader:

        # Add to the total vote count
        total_votes = total_votes + 1

        # Get the candidate name from each row.
        candidate_name = row[2]

        # If the candidate does not match any existing candidate add it to the candidate list
        if candidate_name not in candidate_options:

            # Add the candidate name to the candidate list.
            candidate_options.append(candidate_name)

            # And begin tracking that candidate's voter count.
            candidate_votes[candidate_name] = 0

        # Add a vote to that candidate's count
        candidate_votes[candidate_name] += 1

I believe this program would be an excellent fit for your election commission because it is quick, simple to edit, and provides simple, streamlined information. 
