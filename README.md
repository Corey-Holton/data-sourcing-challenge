# Movie Review Data Analysis

This project retrieves and processes movie review data from The New York Times (NYT) and The Movie Database (TMDB) APIs. The script fetches movie reviews from NYT, searches for these movies in TMDB, retrieves additional details, and then merges and cleans the data for further analysis.

## Setup and Requirements

### Dependencies

The following libraries are required to run the script:
- `requests`
- `time`
- `dotenv`
- `os`
- `pandas`
- `json`

## Environment Variables
Create a .env file in the root directory of your project and add the following environment variables:

NYT_API_KEY=your_nyt_api_key

TMDB_API_KEY=your_tmdb_api_key


Replace your_nyt_api_key and your_tmdb_api_key with your actual API keys for The New York Times and The Movie Database, respectively.

## Script Overview
1. Import Required Libraries and Set Up Environment Variables
The script starts by importing necessary libraries and setting up environment variables from the .env file.

2. Access the New York Times API
The script accesses the NYT API to retrieve movie reviews containing "love" in the headline. It filters for movie reviews in the "Movies" section and sorts them by the newest.

3. Retrieve Movie Reviews
The script loops through pages of the NYT API results, retrieving reviews and storing them in a list.

4. Convert Reviews to DataFrame
The list of reviews is converted to a Pandas DataFrame for easier manipulation and analysis.

5. Process Review Titles
Extracts the movie title from the review headlines for querying the TMDB API.

6. Access The Movie Database API
The script prepares queries for the TMDB API to search for the movies using the extracted titles.

7. Retrieve Movie Details
For each movie title, the script retrieves detailed information from TMDB and stores it in a list.

8. Convert Movie Details to DataFrame
The list of movie details is converted to a Pandas DataFrame.

9. Merge and Clean the Data
The script merges the NYT reviews and TMDB movie details DataFrames on the movie title and cleans the data by removing unwanted characters and duplicate rows.

10. Export Data to CSV
The final cleaned DataFrame is exported to a CSV file named Movie_Data.csv.

Running the Script
Ensure you have your .env file set up with the required API keys.
Run the script in your Python environment:

## References
For this assignment I used a lot of help for askBCS, class material, workgroup with fellow classmates, chat gpt for help with the read me file and Expert learning assistant.

## Conclusion
This script provides a comprehensive approach to retrieving, processing, and merging movie review data from NYT and TMDB APIs, enabling further analysis and insights.

