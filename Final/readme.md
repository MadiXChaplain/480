<h1>Sentiment Analysis Using Naive Bayes Classification Model</h1>
<H2>Introduction</H2>
<H3>Research Question:</H3>
By collecting Twitter Data regarding the Honduran migrant caravan, we can determine the sentiment of affected citizens as positive, negative, or neutral through the Naive Bayes Classification Model.
<H3> Background Information </h3>
There is national conflicting sentiment not only within the United States but Mexico as well reagrding this issue. By utilizing supervised machine learning, we will be able to classify a massive volume of collected Tweets at a proficiency that would be impossible to decipher manually. By sorting the Tweets based on sentiment, as positive, negative, or neutral, we can better understand the scope of the problem and the opinions and voices of those affected by migration occuring across the Southern border or the USA. Instead of one mass collection we will be making two seperate collections using two different words with neutral connotations to see if the attached tweets sway towards more postive or negative sentiment. Additionally, by collecting at two different points in time, we may be able to determing is pubilc sentiment has shifted. By creating a cohesive picture through the collection and classification of Twitter data we can better understand the range of arguments and sentiments, comprehend the severity of this issue as it evolves over time, and would theoretically, be able to provide our insights to decision makers able to institute change derived directly from the public. 
<H3>Analysis of Twitter Data</H3>
By working with a high volume of data we expected inherent data quality issues characteristically found in a large dataset. Our initial collection of 1,529 records revealed duplicate records from tweets that had been favorited,liked, and retweeted. Each of these interaction were treated as seperate records and collected as separate entities despite being identical content. While cleaning our data we had to manually delete repeats in order to maintain credibility in regards to sentiment. We also tried to pick query words that would encapsualte the magnitude of the issue. While our collections returned a wide variety of tweets there is still the possibility of missing values.

<H2> Collection 1: #migrantcaravan </H2>
Our first collection returned 900 records utilizing the key word #migrantcaravan.
Some popular hashtags reflecting Negative sentiment towards the migrant caravan were nationalistic in nature and hostile to the Hondurans occupying the US/Mexico border: #migrantinvasion #buildthewallnow #caravaninvasion
Some popular hashtags reflecting Positive sentiment towards the migrant caravan that were welcoming and hospitable to the Hondurans seeking asylum in the United States: #childrenuprooted #asylum. This wordcloud clusters some of the most popular words returned from the query "migrant caravan". While we found that many of these tweets held negative sentiment, our model categorized the vast majority as neutral. When looking at the wordcloud, some of the most popular words were "walls", "border", and "message". Without the context of a tweet, it would make sense that these words are in fact neutral becuase without context, they are just nuetral descriptors. 
<img src="https://github.com/MadiXChaplain/480/blob/master/Final/worldcloud1.png">

<H2> Collection 2: #Hondurancaravan </H2>
Our second collection returned 629 records utilizing the key word #Hondurancaravan.
Some popular hashtags reflecting Negative sentiment towards the migrant caravan were nationalistic in nature and hostile to the Hondurans occupying the US/Mexico border: #taxpayers #buildthewall #illegalimmigration 
Some popular hashtags reflecting Positive sentiment towards the migrant caravan that were welcoming and hospitable to the Hondurans seeking asylum in the United States: #Refugeeswelcome #HelptheHondurans. The following word cloud clustered the most popular words from this collection. Words such as "throwing", "rocks", and "illegal" indicate a high level of negative sentiment, which was reflected in the models classification of the majority of the tweets being negative. 
<img src="https://github.com/MadiXChaplain/480/blob/master/Final/worldcloud2.png"> 

<H2> Trained Naive Bayes Model Processes </H2>
<h2> Step 1: Collecting the Twitter Data </h2>

[Twitter Collection Process](https://github.com/MadiXChaplain/480/blob/master/Final/search_twitter.xml)

<img src="https://github.com/MadiXChaplain/480/blob/master/Final/Collect_Tweets.PNG"> 

<h2> Step 2: Convert Tweet Data to Text Data </h2>

[Tweet to Text Conversion Process](https://github.com/MadiXChaplain/480/blob/master/Final/Naive_Bayes_Collection_1.xml)

<img src="https://github.com/MadiXChaplain/480/blob/master/Final/step2.PNG">

<img src="https://github.com/MadiXChaplain/480/blob/master/Final/step3.PNG">

<H2> Step 3: Apply Naive Bayes Model </h2>

[Apply Naive Bayes Process](https://github.com/MadiXChaplain/480/blob/master/Final/Apply%20Model%20Process.xml)

<img src="https://github.com/MadiXChaplain/480/blob/master/Final/step4.PNG">

<H2> Trained Naive Bayes Model Visualizations: Collection 1 </H2>


<img src="https://github.com/MadiXChaplain/480/blob/master/Final/BARGRAPHFINAL.PNG">
<i>Figure 1: Proportion Postive, Neutral, and Negative </i>
<H2> Trained Naive Bayes Model Visualizations: Collection 2 </H2>

<img src="https://github.com/MadiXChaplain/480/blob/master/Final/total_count_Bar_collection2.jpg">


<h2> Justification of Naive Bayes Classification Model and Parameters </h2>
We chose the Naive Bayes Classification Model because we were able to take the collected tweets and format examples of inputs and desired outputs. Our model was able to operate through non-numeric labels to appropriately identify text sentiment as positive, negative, or neutral. After reviewing the data overall our testing data was able to produce the desired output (determination of sentiment) based on the training data labels we provided. Through supervised machine learning, we were able to preemptively label a portion of the initial tweets and manually assign them sentiment teaching the model how to think qualitatively. After processing this data through RapidMiner it was optimized through multiple classification iteration cycles. One we had finished these cycles we also used K-Means clustering to classify tweets in RapidMiner and highlight keywords that were popular in our cluster. Utilizing K-means clustering was a useful supplemental to the Naive Bayes Classification Model. By organizing our returned tweets into a word cloud we were able to visualize teh sentiment of tweets by their assigned position and size within the cluster. The parameters structuring our training and testing data was splitting the data into list partitions. The ratio of training data that we labelled was 0.1 and the ratio of testing data we left unlabelled was 0.9.


<h2> Conclusions and Limitations </h2>
We made two collections, based off of the relatively nuetral query words "MigrantCaravan" and "HonduranCaravan". There was disparity among the collected tweets with the overwelming majority of the collected tweets being classified as either negative or nuetral. It was likely that there was an overfitting problem in our training data, as the returned kappa was 1.00 and accuracy was 100%. However, by scanning the predicted label tweets manually, we saw that there was validity in our model. In our post-analysis, we supplemented the models returned predicted labels with an additional sentiment analysis tool. We utilized Python NLTK Text Classification to verify our models accuracy. In the visualizations below, it is evident that our model outperformed the Python NLTK Text Classification tool on both positive and negative sentiments. In applying the K-Means Clustering Model to classify tweets, we were unable to group them into more than one category. After troubleshooting many times, we were unable to remediate the issue, and were left with one wordcloud. Despite this limitation, we were still able generate a wordcloud that provided an overview of the most popular words that were used in the collected tweets.  

<H3> The Naive Bayes Model outperformed the Python NLTK Tool for Classifying Negative Sentiment:</h3>
<img src="https://github.com/MadiXChaplain/480/blob/master/Final/Python%20Analysis%20Negative.PNG">
<img src="https://github.com/MadiXChaplain/480/blob/master/Final/negativetweet.PNG">

<H3> The Naive Bayes Model outperformed the Python NLTK Tool for Classifying Positive Sentiment:</h3>
<img src="https://github.com/MadiXChaplain/480/blob/master/Final/Python%20Analysis%20Positive.PNG">
<img src="https://github.com/MadiXChaplain/480/blob/master/Final/positive%20tweet.PNG">
