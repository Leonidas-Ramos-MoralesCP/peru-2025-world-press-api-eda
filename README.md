# peru-2025-world-press-api-eda
What did the world’s most important newspapers (like NYT) report about Peru in 2025? (¿Qué reportaron los periodicos más importantes (como el NYT) sobre el Perú en el 2025?) 

Countries like Peru care about how they are perceived by major global actors—especially the international news media. Leading outlets often cited by experts include The New York Times (United States), O Globo (Brazil), Le Monde (France), and the BBC (United Kingdom), among others.

This project examines how much—and what type of—coverage Peru received in The New York Times during 2025. The findings can help government, academia, and the private sector better understand Peru’s international image. In future work, the same approach could be extended to additional global media outlets.

To do this, I use the NYT API to collect all 2025 articles about Peru and build a structured database. I then classify the articles with ChatGPT and conduct exploratory data analysis (EDA) to generate summary statistics and visual insights. Finally, I document the full workflow—how the data are retrieved via the NYT API and how the dataset is processed and analyzed.

Process: 
1. Step 1 is to collect the news articles. In this project, I use The New York Times API to retrieve all 2025 articles that match a chosen keyword—here, “Peru.” Before running the script, you must obtain an API key from the NYT Developer Portal. Once you have the key, store it securely (e.g., as an environment variable) and use it in the Google Colab notebook. You can find the script for this case here:
        
https://github.com/Leonidas-Ramos-MoralesCP/peru-2025-world-press-api-eda/blob/main/api_nyt.py

You can find the raw data—containing all articles about Peru published in 2025—here after running the script: 

https://github.com/Leonidas-Ramos-MoralesCP/peru-2025-world-press-api-eda/blob/main/NYT_Peru_2025_Raw_Data.xlsx 

I removed two articles from the raw dataset because they contained the word “peruse,” which is a verb and not a reference to the country Peru. You can find the last dataset here:

https://github.com/Leonidas-Ramos-MoralesCP/peru-2025-world-press-api-eda/blob/main/NYT_Peru_2025_Processed%20Data.xlsx 

3. Step 2 is analyze this dataset. First at all we 
