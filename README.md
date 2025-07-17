# Spotify Listening Habits Analysis 🎧

![Status](https://img.shields.io/badge/Status-In_Progress-yellow)

## 📂 Project Overview

This project is an exploratory data analysis (EDA) of my personal Spotify streaming history. By leveraging data provided by Spotify, I aim to uncover patterns, trends, and insights into my own listening habits. The entire process follows a structured data science workflow, from data loading and cleaning to analysis and visualization, all documented within a Jupyter Notebook.

## 🎯 Key Questions & Objectives

The primary goal is to answer specific questions about my listening behavior. The analysis is divided into two main parts, based on the separation of "listened-to" tracks from "skipped" tracks.

### Main Analysis (Listened Tracks)
- Who are my top 10 most-listened-to artists and what are my top 10 songs?
- What are my peak listening times? (Analysis by hour and day of the week)
- How does my listening activity change over the months of the year?
- What is the average duration of the tracks I listen to?

and additional ones to be defined

### Secondary Analysis (Skipped Tracks)
- Who are the artists I skip the most?
- Is there a pattern in the tracks that are skipped?

##  🔀 Workflow

This project follows a structured and modular workflow:

1.  **Data Loading:** A custom function loads multiple JSON files (`StreamingHistory_music*.json`) and merges them into a single Pandas DataFrame.
2.  **Data Preprocessing:** A dedicated pipeline function cleans the data by:
    - Converting `endTime` to a proper datetime format.
    - Engineering new features like `secondsPlayed` and `minutesPlayed`.
    - Checking for and removing any null values.
3.  **Data Separation:** The preprocessed dataset is strategically split into two distinct DataFrames:
    - `listened_df`: Contains tracks played for more than 30 seconds, serving as the primary dataset for analysis.
    - `skipped_df`: Contains tracks played for 30 seconds or less, used for a separate analysis of skipping behavior.
4.  **Exploratory Data Analysis (EDA):** *(In Progress)* This stage involves deep-diving into the `listened_df` to answer the key questions defined above through data manipulation and visualization.
5.  **API Integration:** *(Future Step)* Enrich the dataset with audio features (e.g., danceability, energy, valence) using the Spotify API.

## 🛠️ Tech Stack

- **Language:** Python
- **Libraries:** Pandas, Matplotlib, Seaborn, Glob
- **Environment:** Google Colab / Jupyter Notebook

## 🚀 How to Run

1. **Request your Spotify data**  
   Go to [Spotify's Privacy Page](https://www.spotify.com/account/privacy/) and request your streaming history.  
   Spotify will email you a download link — this may take a few days.

2. **Open the notebook on Google Colab**  
   The notebook is configured to run on Google Colab. Simply open the `.ipynb` file as indicated in the repository.

3. **Upload your Spotify data**  
   In the first cell of the notebook, you’ll be prompted to upload your `StreamingHistory_music*.json` files (you can upload multiple files).

4. **Run the analysis**  
   Execute the cells one by one to process your listening history and generate personalized insights.

## 📊 Current Status & Next Steps

- [x] Data Loading and Merging
- [x] Data Cleaning and Preprocessing
- [x] Strategic Separation of Listened vs. Skipped Tracks
- [ ] **Next:** Perform Exploratory Data Analysis (EDA) on the `listened_df`.

## ✒️ Author

Created by **Sarah Fernanda**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sarahfernandadc/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/sarahfernandadc)
