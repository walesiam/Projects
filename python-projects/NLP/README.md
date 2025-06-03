**British Airways Customer Review Analysis: Uncovering Sentiment**

**Project Overview**
This project provides a comprehensive analysis of British Airways customer reviews using advanced Natural Language Processing (NLP) techniques to extract valuable insights by combining sentiment analysis with topic modeling. This analysis empowers British Airways (or any airline) to enhance customer experience, optimize services, and address critical areas for improvement.

**Key Features & Techniques**
Data Acquisition & Preprocessing:
Loaded a dataset of British Airways customer reviews.
Performed robust text cleaning, including removal of irrelevant strings, lowercasing, punctuation removal, lemmatization and stop word elimination, ensuring high-quality input for NLP models.

**Sentiment Analysis with Hugging Face Transformers**:
Utilized a pre-trained distilbert-base-uncased-finetuned-sst-2-english model from Hugging Face Transformers for accurate sentiment classification.
Calculated granular "negative score" and "positive score" probabilities for each review.
Categorized reviews into binary "positive" (1) or "negative" (0) ratings based on dominant sentiment.

**Topic Modeling with BERTopic**:
Applied BERTopic, a state-of-the-art topic modeling technique separately to positive and negative reviews. This allows for nuanced discovery of themes specific to each sentiment.
Identified dominant topics within positive feedback (e.g., seat comfort, efficient boarding, friendly staff) and negative feedback (e.g., flight delays, poor customer service, uncomfortable cabins).

**Insightful Visualizations**:
Generated bar plots to visualize the overall distribution of positive vs. negative sentiments.
Enabled the creation of Word Clouds for identified topics, providing intuitive visual summaries of the most frequent keywords in each theme.

**Major Results & Insights**
**Sentiment Distribution**: A significant portion of the reviews were identified as negative (approximately 72.8%), highlighting critical areas for attention, while 27.2% were positive, indicating strengths to be leveraged.

**Common Negative Themes**: Uncovered prevalent issues such as:
Customer Service: Frequent complaints regarding staff attitude and responsiveness.
Flight Disruptions: Numerous mentions of delays and cancellations.
Aircraft Condition: Feedback on older aircraft and lack of modern amenities.
Baggage Handling: Concerns related to lost or delayed luggage.

**Recurring Positive Themes**: Identified areas where British Airways consistently performs well, including:
Seat Comfort: Positive remarks about seat design and legroom.
Efficient Boarding: Smooth and well-organized boarding processes.
Lounge Experience: Appreciation for the quality of airport lounges.

**Actionable Business Intelligence**: The insights derived from this analysis can directly inform strategic decisions, such as:
Prioritizing improvements in customer service training and operational efficiency.
Targeting specific pain points in negative feedback to enhance customer satisfaction.
Reinforcing successful aspects of the customer experience based on positive sentiment.
