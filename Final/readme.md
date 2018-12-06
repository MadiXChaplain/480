<h1>Sentiment Analysis Using Naive Bayes Classification Model</h1>
<H2>Introduction</H2>
<H3>Research Question:</H3>
By collecting Twitter Data regarding the Honduran migrant caravan, we can determine the sentiment of affected citizens as positive, negative, or neutral through the Naive Bayes Classification Model.
<H3> Background Information </h3>
By utilizing supervised machine learning, we will be able to classify a massive volume of collected Tweets at a proficiency that would be impossible to decipher manually. By sorting the Tweets based on sentiment, as positive, negative, or neutral,  we can better understand the scope of the problem and the opinions and voices of those affected by this migration. Instead of one mass collection we will be collecting Twitter data throughout the week as the situation progresses to see if public sentiment has shifted. There is national conflicting sentiment not only within the United States but Mexico as well in how to solve this issue. By creating a cohesive picture through the collection and classification of Twitter data we can better understand the range of arguments and sentiments, comprehend the severity of this issue as it evolves over time, and provide our insights to decision makers able to institute change derived directly from the public. 
<H3>Analysis of Twitter Data</H3>
By working with a high volume of data we expected inherent data quality issues characteristically found in a large dataset. Our initial collection of 1,529 records revealed duplicate records from tweets that had been favorited,liked, and retweeted. Each of these interaction were treated as seperate records and collected as separate entities despite being identical content. While cleaning our data we had to manually delete repeats in order to maintain credibility in regards to sentiment. We also tried to pick query words that would encapsualte the magnitude of the issue. While our colelctions returned a wide variety of tweets there is still the possibility of missing values.

<H2> Collection 1: #migrantcaravan </H2>
Our first collection returned 900 records utilizing the key word #migrantcaravan.
Some popular hashtags reflecting Negative sentiment towards the migrant caravan were nationalistic in nature and hostile to the Hondurans occupying the US/Mexico border: #migrantinvasion #buildthewallnow #caravaninvasion
Some popular hashtags reflecting Positive sentiment towards the migrant caravan that were welcoming and hospitable to the Hondurans seeking asylum in the United States: #childrenuprooted #asylum
<img src="https://github.com/MadiXChaplain/480/blob/master/Final/worldcloud1.png">

<H2> Collection 2: #Hondurancaravan </H2>
Our second collection returned 629 records utilizing the key word #Hondurancaravan.
Some popular hashtags reflecting Negative sentiment towards the migrant caravan were nationalistic in nature and hostile to the Hondurans occupying the US/Mexico border: #taxpayers #buildthewall #illegalimmigration 
Some popular hashtags reflecting Positive sentiment towards the migrant caravan that were welcoming and hospitable to the Hondurans seeking asylum in the United States: #Refugeeswelcome #HelptheHondurans
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

<img src="https://github.com/MadiXChaplain/480/blob/master/Final/PIECHART.PNG">

<img src="https://github.com/MadiXChaplain/480/blob/master/Final/BARGRAPHFINAL.PNG">

<H2> Trained Naive Bayes Model Visualizations: Collection 2 </H2>

<img src="https://github.com/MadiXChaplain/480/blob/master/Final/total_count_Bar_collection2.jpg">

<img src="https://github.com/MadiXChaplain/480/blob/master/Final/total_count_collection_2_pie.png">

<h2> Justification of Naive Bayes Classification Model and Parameters </h2>
We chose the Naive Bayes Classification Model because we were able to take the collected tweets and format examples of inputs and desired outputs. We plan to train our model through non-numeric labels to appropriately identify sentiment. If the model performs correctly, it will produce the desired output (determination of sentiment) when given new sets of collected Twitter data. Through supervised machine learning we can label a portion of the initial tweets and manually assign them as negative, positive, or neutral sentiment. After processing this data through RapidMiner it can be optimized through multiple classification iteration cycles. We may  also use K-Means clustering to classify tweets in RapidMiner to see which keywords are most popular in each cluster. This will be a useful supplement to the Naive Bayes Classification Model because it can organize our returned tweets, and aid in visualizing the sentiment of tweets by their assigned position in different clusters.   

<h2> Conclusions and Limitations </h2>



