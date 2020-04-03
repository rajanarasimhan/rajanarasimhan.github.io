Here I made a dataset called sale.csv. It is dataset which shows product sold vs time. There are five columns in it. The rows are Time(So basically 0 is first half of Jan, 1 is second half of Jan, 2 is first half of February, 4 is the second half and so on), s(Quantity sold in Train set in a particular interval, ef(If the company sold way more product than its forecast then it is 1 else it is 0), rand(randomly generated for test set) and Sales(Quantity sold in Train and Test set). It is skewed dataset as &#39;ef&#39; will be rarely 1 as forecast is done by professional and it will only extent in case of unexpected events.

**Classifier**

So XGBoost being the best classifier I applied it and got 75 percent accuracy and I evaluated the classifier and the results were as follows.

Accuracy: 0.75

Mis-Classification: 0.25

Sensitivity: 0.17

Specificity: 0.94

Precision: 0.94

 Now I started tuning the parameters and I found out for learning rate =0.1, n estimators=4000, max depth=3, min child weight=1, gamma=0, subsample=0.9, colsample bytree=0.8,scale pos weight=6(In my dataset) my classifier was evaluavted as follows

Accuracy: 0.88

Mis-Classification: 0.12

Sensitivity: 0.67

Specificity: 0.94

Precision: 0.94

**Future prediction**

Here I tried to predict see pattern of sales in my dataset. I used exponential shift to see pattern. Here if alpha is between 0.35 to 0.6 we can see some patterns. If alpha is less than 0.35 graph is very vague, more than 0.6 it kind of traces the graph.

Check out the code and dataset at:

[https://github.com/rajanarasimhan/homemade-dataset](https://github.com/rajanarasimhan/homemade-dataset)
