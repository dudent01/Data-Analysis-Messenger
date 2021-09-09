# Data-Analysis

This is a repository for my Jupyter notebooks dedicated to exploring my Facebook Messenger chat data.

***Messenger Analysis*** contains exploratory data analysis of my Facebook Messenger chat data, as well as my explanations of the observed trends. Here I integrate multiple data files into a common pandas dataframe, which contains timestamped messages and information about the message, message senders and conversations from which each message was taken.

I also applied the NLTK SentimentIntensityAnalyzer to find the sentiment of each message.

After that, I began exploratory data analysis on the data, using the **pandas**, **matplotlib** and **seaborn** libraries.
First I looked at how many messages I have received from senders of various majors and of various locations of residence, to provide context for the further analysis.
Most of the exploratory data analysis involves investigating how various features of the message and of the message sender correlate with the sentiment of the message.

I opened this discussion with an exploration of how both the sender's major and the sender's residence impacts the sentiment of the message. I explored how the combination of the two factors influences sentiment of the message. Then I resumed this exploration by observing how these relationships change through time (years and months). Since all of the messages were sent when I was either a high school senior, a college student, or a recent graduate, I accounted for academic year when analyzing messages. I analyzed how academic standing (and academic standing relative to me) correlates with sentiment as well, and how that changes throughout the years.

I then analyzed how the length of the message corresponds to sentiment and discovered that shorter messages are more likely to be neutral, although this measurement might be more indicative of how sentiment is computed by the nltk library.

Then I explored the time series of my own sentiments, and I used rolling averages to explore trends at various granularities.

Finally, I computed the waiting times between messages in each conversation.

*Note: the analysis would be significantly improved if I used significance testing to establish confidence in the discovered correlations.*

***Messenger Learning*** continues the exploration, but now with the use of machine learning approaches. For this I used **scikit-learn** and **tensorflow.keras**. I began by cleaning the data and introducing dummy variables to prepare it for use in machine learning algorithms.

I used logistic regression to predict the year at which a sender entered college.

Then I used **principal component analysis** to represent the data, and explored the resulting scatterplot to get an intuition for the meaning of the axis. My intuition was successful when I viewed the correlations of the components with the original data features.

Then I used a neural network to predict whether a given message was sent by me or sent by someone else. I made sure to check for the balance in the data set beforehand.

Then I  developed a simpler model using my knowledge of the dataset to determine whether a message was sent by me.
