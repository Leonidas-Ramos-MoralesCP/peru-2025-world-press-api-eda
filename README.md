# What did the world’s most important newspapers (like NYT) report about Peru in 2025? 
# (¿Qué reportaron los periodicos más importantes (como el NYT) sobre el Perú en el 2025?) 

1. PROBLEM:

Countries like Peru care about how they are perceived by major global actors—especially the international news media. Leading outlets often cited by experts include The New York Times (United States), O Globo (Brazil), Le Monde (France), and the BBC (United Kingdom), among others.

This project examines how much—and what type of—coverage Peru received in The New York Times during 2025. The findings can help government, academia, and the private sector better understand Peru’s international image. In future work, the same approach could be extended to additional global media outlets.

To do this, I use the NYT API to collect all 2025 articles about Peru and build a structured database. I then classify the articles with ChatGPT and conduct exploratory data analysis (EDA) to generate summary statistics and visual insights. Finally, I document the full workflow—how the data are retrieved via the NYT API and how the dataset is processed and analyzed.

2. PROCESS: 

2.1. Step 1 is to collect the news articles. In this project, I use The New York Times API to retrieve all 2025 articles that match a chosen keyword—here, “Peru.” Before running the script, you must obtain an API key from the NYT Developer Portal. In this case, the API key is free—you just need to sign up on the developer site and generate one.  Once you have the key, store it securely (e.g., as an environment variable) and use it in the Google Colab notebook. You can find the script for this case here:
        
https://github.com/Leonidas-Ramos-MoralesCP/peru-2025-world-press-api-eda/blob/main/api_nyt.py

You can find the raw data—containing all articles about Peru published in 2025—here after running the script: 

https://github.com/Leonidas-Ramos-MoralesCP/peru-2025-world-press-api-eda/blob/main/NYT_Peru_2025_Raw_Data.xlsx 

I removed two articles from the raw dataset because they contained the word “peruse,” which is a verb and not a reference to the country Peru. You can find the last dataset here:

https://github.com/Leonidas-Ramos-MoralesCP/peru-2025-world-press-api-eda/blob/main/NYT_Peru_2025_Processed%20Data.xlsx 

2.2. Step 2 focuses on analyzing the dataset. First, I wrote a prompt for ChatGPT with two tasks: (1) classify the articles into thematic categories and (2) calculate how many articles were published each month. The final prompt was as follows:

Role: Act as a data analyst and text mining expert.Context: I am a political scientist analyzing a dataset of 41 New York Times articles published in 2025.
Task 1: Text Classification
Source Data: Use the text content found in Column B and Column C.
Action: Classify these 41 articles into the following 6 categories that you consider. For example news about the Pope. 
Output: Provide a structured table (formatted for Excel) that maps each news item to its assigned category.
Task 2: Temporal Analysis
Source Data: Use the date information in Column A.
Action: Calculate the frequency of articles published per month throughout 2025.
Output: Provide a summary table in Excel showing the month and the corresponding count of articles.

The results are compiled in the following Excel file: 

https://github.com/Leonidas-Ramos-MoralesCP/peru-2025-world-press-api-eda/blob/main/NYT_Peru_2025_TextMining_Outputs_.xlsx

Then I asked ChatGPT to identify the most frequent words in the titles and descriptions of these articles. This is the prompt I used:
Role: Act as a data analyst and expert in text mining and Natural Language Processing (NLP).Context: I am a political scientist analyzing a dataset of 41 New York Times articles from 2025.  Task 3: Keyword Frequency & NLP Cleaning. Source: Combine text from Column B and Column C.Action: 1.  Perform a word count analysis across the entire corpus (all 41 news items). 2.  Crucial: Filter out all "stopwords" (common words like: the, and, of, in, to, a, is, etc.). 3.  Focus only on meaningful nouns, verbs, and adjectives. Output: A table in Excel showing the Top 20 most frequent keywords and their respective 

The results are summarized in the following Excel file:
https://github.com/Leonidas-Ramos-MoralesCP/peru-2025-world-press-api-eda/blob/main/NYT_Peru_2025_TextMining_Outputs_.xlsx  

3. RESULTS:

According to our script, The New York Times published 41 articles in 2025 that were directly related to Peru. Most of this coverage focused on the election and life of Pope Leo XIV. 

ChatGPT automatically generated six categories. The two categories with the highest number of articles were Religion & Vatican and Culture & Lifestyle. The first is largely driven by coverage of the election of Pope Leo XIV, while the second focuses on arts, travel, and lifestyle-related stories connected to Peru.

<img width="751" height="452" alt="image" src="https://github.com/user-attachments/assets/11c50664-9eba-4787-9abc-e0389028cedc" />

The month in which The New York Times published the most articles about Peru was May 2025. This peak coincides with the election of Pope Leo XIV, who had obtained Peruvian citizenship years earlier. Most of the articles published that month focused on this connection.

<img width="751" height="452" alt="image" src="https://github.com/user-attachments/assets/6c366b16-88df-4b23-a2fd-1e5ffe2bf0a3" />

The most frequent words are “Peru” and “Pope”: 

<img width="751" height="452" alt="image" src="https://github.com/user-attachments/assets/9517f44a-d86f-49f2-a4ea-364bf9829cf3" />






