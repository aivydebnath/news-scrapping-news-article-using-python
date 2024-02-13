#  Objective 
The primary goal of this project was to gather and analyze news articles related to the Israel-Hamas conflict from various news sources, including Al Jazeera, CNN, 
Business Insider, NDTV, and Republic World. The focus was on extracting relevant content, performing sentiment analysis, identifying top keywords, and generating 
word clouds to gain insights into the coverage provided by these news outlets for a month.
# Data Collection 

  • Al Jazeera: Utilized web scraping techniques with Selenium to retrieve news articles from Al Jazeera's website, considering articles published in the current 
  year for 30 days.
      a. I got the 30-day article after clicking “Show more” 50 times. Since for each day, we have multiple news articles present on each website
      b. The next step is to go to each URL/link and get the article. So that I have collected the article from each website
      c. Last step, I saved the entire text article in a text file with the headlines
  
  • CNN: Collected news articles from CNN's Middle East live news section for the last 30 days using web scraping.
      a. To get the data for a month I had to change the base URL with the dates I required articles for
      b. The next part I have done is to go to each link and get the article. For this, I used a loop and ran it 30 times while changing the dates
      c. Last step, I exported the entire text article for each website to one text file
  • Business Insider: Extracted news articles using web scraping techniques, specifically targeting articles related to the Israel-Hamas conflict.
      a. First, I ran a loop from 1 to 23 to get the data for a month. My first job was to get all the links for the articles
      b. Then, filter out only Hamas or Israel news articles and run a loop to get the article for each URL
      c. Initially, I got results for each iteration and liked each article summary in one iteration
      d. Lastly, export all the iterated articles and save it in a text file
  • NDTV: Scraped news articles from NDTV's dedicated page for the Israel-Hamas conflict.
      a. I went to the live news website and exported all URLs for that particular page only. I checked they did not have
      many articles about the Israel-Hamas conflict, all the articles they have on a single page contain the data for a month
      b. So, I exported the hrefs under the div tag and then ran a loop to go to each link and extract the article
      c. Then, accumulate all the articles in one text file
  • Republic World: Extracted relevant news articles from Republic World's website, focusing on the ongoing conflict.
      a. Again, the republic world does not much have data for the conflict
      b. So, I went to all the headlines I had on one page. Since they have an entire month of data in one page
      c. Then, extract the paragraph for each headline
      d. Exported all of them in one text file
  Data Processing 
    • Cleaned and processed the extracted text content to prepare it for analysis. Removed unnecessary headlines, time duration of the article
    • Implemented sentiment analysis using TextBlob to quantify the overall sentiment of each news source.
    • Utilized NLTK for keyword extraction, considering the top 15 keywords from each news source.
    • Generated word clouds to visually represent the most frequent words in the news content, excluding common and irrelevant terms like said, facebook etc.
    • Topic Modelling using LDA (Latent Dirichlet Allocation):
        ▪ The code reads the content from the "all_content.txt" file and tokenizes the documents.
        ▪ It then creates a dictionary and a bag-of-words corpus for the documents.
        ▪ LDA is applied to identify topics in the corpus. The most representative words for each topic are printed.
        ▪ The distribution of topics across documents is visualized using a heatmap.
        ▪ Each document is associated with its dominant topic and probability of association.
    • Coherence Score Calculation:
        ▪ The code calculates the coherence score for the LDA model, providing a measure of how well-defined and interpretable the topics are.
    • Topic Modelling using LSA (Latent Semantic Analysis):
        ▪ The code applies Latent Semantic Analysis (LSA) using the TF-IDF matrix to find the most important terms for each topic.
        ▪ Top terms for each topic are displayed.
    • Word Embeddings with Word2Vec:
        ▪ Word2Vec is used to create word embeddings for the tokenized documents.
        ▪ Similar words for the term 'war' are found and printed.
# Critical Output 
Sentiment scores are typically numerical values ranging from negative to positive. The sentiment analysis, keyword extraction, and word clouds provide valuable insights 
into the focus and tone of each news outlet's coverage. Here's a general interpretation for positive sentiment since all our article got positive scores:
Positive Sentiment (Score > 0): A positive sentiment score indicates that the overall tone of the text is positive. It suggests that the language used in the content 
expresses favourable opinions, satisfaction, or optimism.
For our assignment, below is the sentiment scores of all the 5 news articles and top keywords:
Al Jazeera 
    Sentiment Score for Al Jazeera: 0.027930978287730102
    Interpretation: The sentiment score is slightly positive, indicating a generally neutral sentiment.
    Top Keywords: The main topics revolve around the conflict in Gaza, involving Israel, Hamas, war, and military actions.
CNN 
    Sentiment Score for CNN: 0.01811006539756538
    Interpretation: The sentiment score is also positive but relatively lower, suggesting a more neutral sentiment.
    Top Keywords: The keywords highlight the focus on Gaza, Israel, and related topics, with additional mentions of CNN and specific dates.
Business Insider 
    Sentiment Score for Business Insider: 0.0379680136898772
    Interpretation: The sentiment score is positive, indicating a somewhat positive tone.
    Top Keywords: Keywords focus on specific elements of the conflict, including Hamas, Israel, war, and military-related terms.
NDTV 
    Sentiment Score for NDTV: 0.0689096720192778
    Interpretation: The sentiment score is higher, suggesting a more positive overall sentiment.
    Top Keywords: The keywords highlight Gaza, Israel, Hamas, war, and include terms like hostages and attacks.
Republic World 
    Sentiment Score for Republic World: 0.033577891043603446
    Interpretation: The sentiment score is positive, indicating a generally neutral sentiment.
    Top Keywords: Keywords include Israel, Hamas, Gaza, IDF (Israel Defense Forces), war, and political figures.
Top Words for Each Topic 
        Topic 1 is characterized by words like Gaza, Israel, war, Hamas, and Palestinian, suggesting a focus on the Israeli-Palestinian conflict.
        Topic 2 includes words such as the US, sea, red, houthis, Yemen, and shipping, indicating a focus on maritime issues and possibly the Yemen conflict.
        Topic 3 involves words like Israel, Africa, South, court, genocide, and justice, suggesting a legal or international justice-related theme.
        Topic 4 includes terms like Jazeera, Al, West Bank, occupied, reporting, and raids, indicating a focus on news reporting and possibly conflict-related news.
        Topic 5 is associated with words like Minister, Netanyahu, Prime, Hamas, Benjamin, Blinken, and President, suggesting political figures and diplomatic 
        relations.
Similar Words for Specific Terms 
      For the term 'war,' the similar words include 'end,' 'coverage,' 'israel,' and 'miss,' possibly reflecting the diverse aspects of war coverage and its 
      implications.
      For 'Israel,' similar words include 'accused,' 'stopped,' 'campaign,' and 'blaming,' indicating various perspectives or events related to Israel.
      For 'Hamas,' similar words include 'escalated,' 'assault,' and 'offensive,' reflecting the intensification of conflict and offensive actions.
# Conclusion 
  The project has effectively gathered, processed, and analyzed news articles from reputable sources, shedding light on the Israel-Hamas conflict. Through 
  sentiment analysis, keyword extraction, and word clouds, we've gained valuable insights into the thematic focus and tonal nuances of each news outlet's 
  coverage. The chosen methodology offers a comprehensive approach to unraveling the media landscape surrounding this enduring conflict.
  The analysis has unveiled a diverse array of topics, ranging from the Israeli-Palestinian conflict and maritime issues to legal considerations, news reporting, 
  and prominent political figures. The coherence score of 0.5336 signals a moderate level of consistency in the identified topics.
  It's crucial to emphasize that our interpretation is grounded in the identified topics and their associated words, providing nuanced insights into the 
  prevailing themes within the corpus
