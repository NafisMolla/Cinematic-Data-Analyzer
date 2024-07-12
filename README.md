# Large-Scale Cinematic Data Processing with Spark in Scala

## Overview
This project consists of a series of Scala-based Apache Spark applications designed to process and analyze large-scale movie ratings datasets. The applications cover various analytics tasks, providing insights into user behavior, movie popularity, and comparative movie analysis.

## Applications

### Task 1: Maximum Rating Identification
- **Objective:** Identify the highest ratings for each movie and list the users who provided these ratings.
- **Method:** Reads a CSV file where each line contains a movie title followed by user ratings. The application finds the maximum rating for each movie and the corresponding user indices.
- **Output:** A CSV file listing each movie along with the users who gave the highest ratings.

### Task 2: Total Rating Count
- **Objective:** Calculate the total count of non-empty ratings across all movies.
- **Method:** Uses a long accumulator to aggregate the count of non-empty ratings found in each line of the dataset.
- **Output:** A single-value file representing the total count of ratings.

### Task 3: User-Specific Rating Counts
- **Objective:** Compute the total number of ratings submitted by each user.
- **Method:** Processes each line of ratings, maps each rating to its corresponding user, and reduces by key to count ratings per user.
- **Output:** A CSV file where each line contains a user ID and their total ratings count.

### Task 4: Comparative Analysis of Movie Pairs
- **Objective:** Analyze pairs of movies to determine the count of users who rated both movies the same.
- **Method:** Utilizes Cartesian product to compare every pair of movies, filters pairs to ensure unique comparisons, and counts the number of matching ratings.
- **Output:** A CSV file listing each unique movie pair along with the count of matching ratings.

### SparkWC: Word Count Application
- **Objective:** Perform a basic word count on a given text file.
- **Method:** Splits lines into words, maps each word to a count, and reduces by key to sum occurrences.
- **Output:** A CSV file where each line contains a word followed by its count.

## Technical Details
- **Language:** Scala
- **Framework:** Apache Spark
- **Data Size:** Each file processed contains over 10,000 entries, illustrating the application's capability to handle large datasets efficiently.
- **Environment:** Developed and tested in a distributed Spark environment, ensuring scalability and performance.
