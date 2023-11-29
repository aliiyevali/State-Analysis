## Introduction

As an aspiring data analyst and scientist poised to graduate soon, my journey into the professional world is marked by a crucial decision: selecting the ideal state in the USA to live in and start my career. This decision, pivotal in shaping my professional and personal life, led me to leverage my analytical skills to make an informed choice. This document encapsulates the comprehensive analysis undertaken to understand sentiments about different states in the USA, providing insights into which locations might offer the most favorable conditions to live in for any person like myself.

## Background

The genesis of this project stemmed from a simple yet profound question: "Which states in the USA offer the best conditions to live in?" Initially, I sought answers through conversations with friends. However, I quickly realized that these responses, albeit well-intentioned, were inherently biased. Some friends, driven by the desire to have me closer, portrayed their residing states in a favorable light. It became evident that a more objective, data-driven approach was needed – one that would cut through personal biases to reveal the true sentiment about each state.
In this pursuit, I embarked on a project to analyze and interpret various sentiments associated with different states across the USA. The core of this project is a dataset consisting of comments about each state, paired with sentiment scores ranging from -1 (negative) to 1 (positive). These scores were obtained using the BERT model, a state-of-the-art tool in natural language processing, ensuring a high degree of accuracy and reliability in the sentiment analysis.

## Methodology

The project followed a rigorous methodology:
1. Data Scraping: Collecting a wide array of comments from diverse sources to ensure a comprehensive dataset.
2. Data Cleaning: Processing the gathered data to eliminate noise and ensure its relevance and accuracy.
3. Interactive Application/Widget Development: Creating a user-friendly application that inputs a state name and outputs the top 10 words associated with that state, providing an intuitive understanding of public sentiment.
4. BERT Model Implementation: Utilizing the BERT model to analyze the sentiment of each comment, assigning scores that reflect the positive or negative nature of the sentiments expressed.
5. Statistical Analysis & Comparisons: Employing various statistical methods, including weighted averages, Z-scores, simple means, and categorical analysis, to interpret the sentiment scores effectively.
6. Tableau Dashboard, Graphs and Results: Designing a Tableau dashboard to visually represent the data, facilitating easier discovery of patterns and insights.
The primary goal of this document is to present the results and interpretations derived from this extensive analysis. By doing so, it aims not only to guide my personal decision-making process but also to serve as a valuable resource showcasing how admirable can statistical analysis be in any persons’ life. This project stands as a testament to the power of data in making life-changing decisions. By combining technological prowess with analytical acumen, it showcases how data can be transformed into meaningful insights, guiding us toward informed choices that shape our future.

## Part 1: Scraping

The foundational step in answering the critical question - "Which is the best state to live in?" - involved gathering diverse opinions and insights from the internet. Recognizing the rich and varied discussions on Reddit, I focused my data collection efforts on this platform. I consistently strive to personally acquire my data, the goal is to ensure the data is qualitative, up-to-date, and unbiased for analysis. These criteria were crucial to maintain the integrity and relevance of the analysis.
To ensure the data was qualitative, up-to-date, and unbiased, I employed Selenium for scraping. Reddit, known for its dynamic HTML format, presents challenges that make traditional scraping tools like BeautifulSoup less effective. Selenium, with its ability to interact with dynamic web content, was therefore the tool of choice.
My search on Reddit led to the discovery of 7-8 subreddits, each centered around the recurring theme, "Which is the best state?" These forums provided a wealth of user-generated content, offering diverse perspectives on the topic. I systematically provided each subreddit link to my scraping tool and meticulously extracted the data.
It's important to note that the dataset I compiled is derived from a single, yet rich source of information. Each comment and discussion thread in these subreddits contributed to the dataset, providing a multi-dimensional view of public opinion about different states in the USA.

## Part 2: Data Cleaning & Processing

After collecting a substantial amount of data from various Reddit subreddits, the next critical phase was to clean and process this data. The objective was to transform the raw, unstructured text data into a format that is suitable for analysis and to ensure that it accurately reflects the sentiment of the original comments.
The initial step involved cleaning the text data. This process included removing irrelevant characters, correcting typos, and standardizing the format of the text to ensure consistency across the dataset.
A crucial part of the data cleaning involved creating a new column in the dataset. This column was designed to identify and record the specific state mentioned in each comment. This step is fundamental for comparing and analyzing the data on a state-by-state basis.
Recognizing the limitations of sentiment analysis models in interpreting comments with only state names, I introduced an innovative approach to enhance data quality. Since the original subreddit question was, "Which is the best state?" and some responses included only the name of a state, I appended positive words to these comments. This addition provides necessary context, making it logical and coherent for sentiment analysis. The positive words were carefully chosen to reflect a favorable sentiment, aligning with the context of the subreddit question.

## Part 3: Interactive Application/Widget Development 

The application phase of the project was designed to leverage the power of NLP in conjunction with the machine learning model. The primary intention was to distill the essence of public sentiment into a concise, easily interpretable format. This was achieved by developing an application that identifies and presents the most frequently used words associated with each state, based on the analyzed comments.
NLP Integration: By applying NLP techniques to the comments dataset, I was able to extract key words that recurrently appeared in discussions about each state. This process involved parsing through the text data, identifying significant words, and ranking them based on frequency and relevance.
Application Development The culmination of this analysis was the creation of an interactive application. This user-friendly tool is designed to accept a state name as input and, in response, generate a list of the top 10 words that are most commonly associated with that state in the dataset.
An example of the application's utility can be illustrated with Massachusetts. Upon entering "Massachusetts" as the input, the application returns words like "education", "health care", "schools", and "mountains" among others. These words collectively represent what comes to mind when thinking about Massachusetts.

<img width="837" alt="Screenshot 2023-11-29 at 3 16 05 AM" src="https://github.com/aliiyevali/Stateside-Sentiment-Analysis-Ideal-Destination/assets/147966223/11d543a8-68e3-4c9e-ba35-37686b65197c">

As a resident of Massachusetts, myself, I can attest to the accuracy of the application. It effectively captures and reflects the prevailing sentiments and characteristics associated with the state, as expressed in the Reddit comments.

## Part 4: BERT Model Implementation

Following the scraping of Reddit subreddits focused on discussions about various USA states, the next pivotal phase was the implementation of machine learning (ML). This section outlines the approach and methodologies employed in applying ML techniques to the dataset.
Unsupervised Learning: Given the nature of the data, which lacked predefined labels, the project necessitated the use of unsupervised machine learning techniques. Unsupervised Learning is ideal for discovering hidden patterns or intrinsic structures within unlabeled datasets.
BERT Model: The cornerstone of the machine learning phase was the implementation of the BERT (Bidirectional Encoder Representations from Transformers) pre-trained model. BERT is renowned for its effectiveness in understanding the context of words in text data, making it an excellent choice for sentiment analysis. The BERT model was applied to the dataset, where it analyzed the text of the comments, extracting sentiment scores. These scores represent the emotional tone conveyed in each comment, ranging from positive to negative sentiments.
In addition to providing sentiment scores, the BERT model also categorized the comments based on their sentiment. This categorization was binary, classifying comments as either positive or negative, based on the context and content of the text.

Part 5: Statistical Analysis & Comparisons
Employing various analytical methodologies is crucial to mitigate inherent biases in data analysis. Different approaches can highlight unique aspects of the data, providing a more rounded and unbiased perspective.


### Comparison by Mean

Asking a friend how to compare two groups often elicits a simple response: compare their means. While this approach is intuitive and straightforward, as a data scientist, it's crucial to recognize that it may not always provide a complete picture.
In this project, the first level of comparison involved looking at the mean sentiment scores of each state. This method provided an initial, broad overview of the overall sentiment towards each state.
However, this approach might oversimplify the complexities inherent in the dataset. For instance, the number of records for each state are different and treating in very simple way as comparing only averages might lead to incomplete interpretations.

### Comparison by Weighted averages

In data science, it is acknowledged that there can be weighted differences in groups, which can significantly influence the comparison. These 'weights' refer to the varying significance or value assigned to different elements within a group. An illustrative example can be found in some political debates where the suggestion is made to value the votes of educated people more than those of uneducated individuals. This proposal is essentially about altering the 'weights' assigned to each vote, thereby changing the impact of each individual's opinion based on their education level.
Here is how I calculated weighted averages: 
1.	Counted the number of reviews for each state.
2.	Multiplied the counts by sentiment scores to get a "weight" for each state.
3.	Normalized these weights by dividing by the total sum of all weights to get a weighted average for each state.
In this analysis, state weights are based on comment counts, avoiding bias from individual comment weighting. The volume of comments serves as a proxy for interest in a state. Weighted averages balance sentiment representation, compensating for states with varying comment volumes. This method minimizes distortion from uneven comment distribution, ensuring all states are fairly considered, leading to a more nuanced analysis.
Here are the results:

<img width="483" alt="Screenshot 2023-11-29 at 12 23 54 AM" src="https://github.com/aliiyevali/Stateside-Sentiment-Analysis-Ideal-Destination/assets/147966223/aa4cdd12-c3a4-48c0-9f73-accebded876f">

California has the highest weighted average sentiment score of approximately 0.26333. This number is a relative measure, meaning it is not just the sentiment but the sentiment as a proportion of the total sentiment across all states. The score indicates that California not only received a high sentiment score on average but also that this score is significant in the context of the overall sentiment across all reviews.
Limitations:
Without weighting, states with a very high number of reviews would dominate the average sentiment score, possibly overshadowing smaller states that could have more extreme sentiment scores (either positive or negative) but fewer reviews.
Washington has the top 2 count of reviews with a neutral average sentiment score of 0.5. Rhode Island, on the other hand, has very less reviews with a very positive average sentiment score of 0.6. Without weighting, when calculating the overall sentiment, Washington’s large number of reviews made the overall sentiment appear more neutral, overshadowing the fact that Rhode Island, although with fewer reviews, has a much more positive sentiment.
States with very few comments could have their sentiment scores overly influenced by a small number of reviews. This could distort the overall sentiment analysis by giving undue weight to what might be unrepresentative opinions.
Nebraska has fewer reviews with an average sentiment score that happens to be negative due to a few extremely negative reviews. Without weighting, these few negative reviews significantly bring down the overall sentiment average more than they should, considering their small number relative to the total number of reviews. As I can’t weight or rank comments, this bias is inevitable for weighted averages method. 
Pros of Weighted averages method:
States with many comments don't disproportionately affect the average sentiment score more than states with fewer comments because the sentiment score of each state is considered relative to the total sum of weights, not just the raw sentiment score.
	Using the weighted average approach, Washington is in top2 for review counts reviews with a neutral average sentiment score of 0.5. In a weighted system, these reviews contribute to the overall sentiment in proportion to the total number of reviews and their sentiment scores, so even though Texas has many reviews, it doesn’t overshadow a state like Rhode Island, which has fewer reviews with a sentiment score of 0.6.
The opposite is also True: States with fewer comments don't get an undue influence because their weighted contribution is smaller relative to states with more comments.
Rhode Island has fewer reviews with a high sentiment score of 0.6, in a weighted average system, these reviews would not overly skew the overall sentiment because their weight is proportionate to their share of the total number of reviews. This means that Rhode Island's positive sentiment contributes to the overall average, but it doesn't have an outsized impact just because the sentiment score is high.

### Comparison by Category

Following the weighted average analysis, the project progressed to a categorical analysis. This phase aimed to examine the states based on the sheer number of positive or negative reviews, independent of sentiment scores. 
Unlike previous methods that relied on sentiment scores, this approach centered on quantifying the number of positive and negative reviews for each state. The fundamental question was: "Which state has the highest number of positive or negative reviews?"
By comparing states based purely on the count of positive or negative reviews, this method provided a different viewpoint. It helped to balance the analysis by considering the raw number of sentiments expressed, regardless of the state's online presence or engagement levels.
While categorical analysis offers valuable insights by focusing on the volume of positive or negative reviews, it is important to acknowledge its limitations, especially in the context of internet usage disparities:
Different states have varying levels of internet penetration and activity. States with higher internet usage are likely to generate more comments, which can skew the analysis. This disparity means that the count of positive or negative reviews might not accurately reflect the sentiment towards a state but rather its online activity level. Relying solely on the number of reviews could lead to a misrepresentation of the overall sentiment. States with less internet engagement might have fewer comments, resulting in an underrepresentation of their sentiments in the analysis.

<img width="638" alt="Screenshot 2023-11-29 at 3 18 46 AM" src="https://github.com/aliiyevali/Stateside-Sentiment-Analysis-Ideal-Destination/assets/147966223/e15d68aa-9c42-491f-8b75-1661eb44e9d1">

Therefore, while the categorical analysis provides a different viewpoint, it is crucial to consider these limitations and interpret the findings within the context of internet usage disparities among states.

### Comparison by Z-scores

After exploring various methodologies, including means, weighted averages, and categorical analysis, the project culminated in the use of Z-score analysis. 
Each of the previous methods brought its unique insights but also had inherent limitations, particularly in terms of balancing bias and accurately representing sentiments across different states. Z-score analysis was identified as a method that could address these challenges more effectively.
 	A Z-score measures how many standard deviations an element is from the mean of a dataset. In this context, it was used to determine how far the mean sentiment score of a particular state is from the overall mean of the entire dataset.
By calculating the Z-scores for each state, it became possible to understand the relative position of each state's sentiment in the context of the national sentiment landscape. This method provides a standardized measure, making it easier to compare states with varying numbers of comments and levels of internet engagement.
Z-scores normalize the data, allowing for a fair comparison between states by accounting for differences in sample sizes and variances.
This approach is particularly useful in identifying states that have exceptionally high or low sentiment scores relative to the national average, highlighting outliers that might be of particular interest.

<img width="365" alt="Screenshot 2023-11-29 at 3 19 55 AM" src="https://github.com/aliiyevali/Stateside-Sentiment-Analysis-Ideal-Destination/assets/147966223/dcebfd9d-2092-44e9-98e1-fb873b3f9c2c">

Virginia has the highest z-score, which suggests that it has the most positive sentiment score relative to the other states. If we are to interpret the "best" state as the one with the most positive reviews, then Virginia would be the answer given the data from Reddit.
## Part 6: Tableau Dashboard, Graphs and Results
<img width="1440" alt="State Tableau" src="https://github.com/aliiyevali/Stateside-Sentiment-Analysis-Ideal-Destination/assets/147966223/dd109b36-ccaf-4cf5-b5e1-2491a35fb00d">

### Analytical Dashboard Breakdown

The dashboard presents an intricate analysis of sentiments associated with the states and regions of the USA. Through various visualizations, it offers insights into the comparative sentiment analysis conducted using different statistical measures. Let me delve into each visual element of the dashboard to unpack the findings of my sentiment analysis.

### Header Annotations

At the top of the dashboard, I have highlighted the standout states as per different analytical approaches:
- Best State by Weighted Averages: This signifies the state that emerges as the most favorable when considering the weighted average of sentiment scores. California is identified as the best state according to weighted averages, indicating that when the number of comments is taken into account alongside sentiment scores, California has a strong positive sentiment.
- Best State by Z-Scores: This denotes the state that stands out based on Z-score analysis, indicating its position in terms of standard deviations from the mean sentiment score across all states. Virginia is highlighted here, showing that it has a notably high sentiment score compared to the national average.
- Best State by Number of Positive Reviews: This reflects the state with the highest count of positive sentiment expressions. Again, California appears to be the most positively reviewed state, showcasing its prominence in public opinion.

### Score Comparison Butterfly Bar Chart

This top-left butterfly bar chart serves as a comparative visualization, juxtaposing the weighted averages and Z-scores of each state. The left side, depicted in red, represents the weighted averages, indicating the adjusted mean sentiment scores with respect to the volume of comments. On the right, shown in blue, the Z-scores place each state on a standard scale of deviations from the overall mean sentiment score. This dual-sided chart provides a clear comparative view, highlighting how each state fares in terms of public sentiment when analyzed using these two distinct methods.
For instance, Washington shows a high weighted average sentiment but also a high Z-score, indicating it not only has a volume of positive sentiment but also that sentiment is significantly positive when measured in standard deviations from the mean.
Florida's notable high weighted score alongside a lower z-score indicates that while aspects of the state are highly valued, perhaps for its distinct environmental and cultural attractions, these attributes aren't as pronounced when evaluated against a standard measure. This could imply that Florida's appeal, potentially stemming from its warm climate and natural tourism activities, is particularly appreciated by niche audiences. Since Florida is a very touristy place, we can classify this niche audience as tourists. However, these features might not align with the more general factors favored by people in the USA; we are aware of how Americans complain about Florida. The weighted average doesn't take into account how Florida's performance compares to the other states in terms of variability and distribution, while the Z-score does. Therefore, the Z-score might reveal that what Florida is good at doesn't set it as far apart from other states when considering the full range of metrics and their variation.

### USA State Ranking Map

This central USA state ranking map, where the shades of red represent the Z-scores associated with each state. Darker shades correspond to higher Z-scores, thus indicating a more positive sentiment relative to the national average. This geographical representation allows for an immediate visual assessment of how sentiments are distributed across the country, providing a regional context to the numerical data.
This geographical visualization is useful for quickly identifying regional patterns in the data, where the central states seem to have a lower rank compared to coastal states.
Let's consider the example of technological innovation and business development, metrics often used to evaluate a state's performance. Coastal states like California and New York are known for their bustling tech hubs—Silicon Valley. These areas attract a high level of investment, talent, and create a competitive environment that fosters innovation and economic growth. This concentration of resources and visibility can lead to higher performance metrics in technological advancement, GDP, and job creation.
In contrast, central states may focus more on agriculture, manufacturing, or energy production, industries that are vital but might not scale or attract investment as quickly as the tech sector. The geographical visualization helps highlight this disparity, as coastal states may rank higher due to the agglomeration of cutting-edge industries and the global connectivity that ports and international airports provide.
My opinion is that these regional differences are not just reflections of the present economic landscape but are also deeply rooted in historical development patterns, where coastal states had early advantages due to trade and immigration. These long-standing benefits continue to echo today, translating into higher rankings in various evaluations that often favor modern, service-oriented economies.

### Review Categorizing Butterfly Bar Chart

The butterfly bar chart on the top right compares the number of positive and negative reviews for each state. The left side in blue illustrates the count of positive reviews, whereas the right side in red indicates negative reviews. This chart succinctly summarizes the polarity of sentiments expressed towards each state, offering a clear indicator of which states provoke more positive or negative reactions.
California indeed has a high number of both positive and negative reviews. It makes sense given California's large population and diverse range of services and amenities that would generate a high volume of feedback.

### Top Regions Treemap

The treemap in the middle left categorizes the top regions and represents the sum of Z-scores for each. The size of each box correlates with the cumulative Z-score of the states within that region. Larger boxes with darker shades suggest a stronger positive sentiment in that region. New England is notably prominent, indicating an overall positive sentiment when aggregating the Z-scores of its states.

### Top 3 States Per Region

At the bottom right, we have a bar chart listing the top three states per region according to their Z-scores. This breakdown allows for a focused analysis of regional leaders in public sentiment, offering a ranking within geographical clusters.
It's noteworthy that Rhode Island tops the New England region with a high positive score. Despite being one of the smallest states, it appears to outperform its larger neighbors in this context.

### Reviews By Category Waffle Chart

Lastly, the waffle chart at the bottom left provides a percentage breakdown of all reviews into positive and negative categories. Each small square represents a proportion of the total number of reviews, with red squares indicating negative sentiments and blue squares representing positive ones. The resulting visualization confirms that nearly 60% of all reviews are positive, while 40% are negative, thus giving a quick visual reference to the overall sentiment tilt.
