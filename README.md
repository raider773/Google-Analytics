# Google-Analytics
Clustering, Time Series and Classification on a sample from a Google Analytics Dataset




This Project is based on a sample of a dataset from a google analytics gathering. The objectives of this project were multiple.\
First i analysed the data and make some charts that better represent this dataset.\
In the features.txt file there's a description of the features.\
Then i did some clsutering to group clients and analyse the groups a bit.\
After that i did some classification. I tried to predict whether the client would or would not make a transaction.\
Then i did some time series prediction on the revenue.\
Lastly i used flask to implement both the time series model as well as the classification model, giving a full report.



<img align="left"  width="260" height="260" src="https://user-images.githubusercontent.com/70241561/121459170-23971480-c981-11eb-8d21-0a9a20ba9b36.png"> 



The percentage of nulls was great. I had to drop a lot of columns due to nulls or not giving any information. Also used some imputation techniques. The balance of classes for the classification was 98% for one class and 2% for the other, Instead of using undersampling or oversampling, I trained the model with the real data, use AUC and F1 Score as metrics to compare models and move the threshold. The percentage of classes was so great, if i used some some of sample alteration then i would have changed the data too much.



<p>&nbsp;</p> 
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>



![image](https://user-images.githubusercontent.com/70241561/121459495-c059b200-c981-11eb-8704-b23089161d2b.png)

We can see chrome and desktop are the most used.

<p>&nbsp;</p>
<p>&nbsp;</p>



![image](https://user-images.githubusercontent.com/70241561/121459547-dff0da80-c981-11eb-9f9f-b9bb43baa5b3.png)

The PCA shows classes are not so well separate.

<p>&nbsp;</p>
<p>&nbsp;</p>

![image](https://user-images.githubusercontent.com/70241561/121459664-10d10f80-c982-11eb-8c86-685a7cf867a6.png)

After doing some feature importance with a random forest and an extra trees, we can see time on site, hits and page views are what most influence a prediction for a transaction.

<p>&nbsp;</p>
<p>&nbsp;</p>

For classification i selected a logistic regression model, since it ws the one that performed well.


![image](https://user-images.githubusercontent.com/70241561/121459856-60174000-c982-11eb-82b3-cac4e0ab3020.png)

<p>&nbsp;</p>

![image](https://user-images.githubusercontent.com/70241561/121459914-7ae9b480-c982-11eb-8c22-ac29fedec892.png)

Auc Curve was good, separation of data was ok.

<p>&nbsp;</p>

![image](https://user-images.githubusercontent.com/70241561/121459942-8c32c100-c982-11eb-8908-9273c84a5fd1.png)

A chart with metrics based on threshold

<p>&nbsp;</p>

![image](https://user-images.githubusercontent.com/70241561/121460007-9f459100-c982-11eb-9f11-c6d1b1b825de.png)

set threshold and watch how matrix confusion changed.


<p>&nbsp;</p>

Next i did some time series prediction. I tried a lienar trend with and without months, as well as performed an adfuller test to see the p-values. Stationality was pretty static, and months got high p-values so they didn't add anything to the prediction. I used prophet and it performed ok, so i selected that model and save it for using it with flask.

<p>&nbsp;</p>

![image](https://user-images.githubusercontent.com/70241561/121460251-06634580-c983-11eb-8978-00cecae3926e.png)

Stationality

<p>&nbsp;</p>

![image](https://user-images.githubusercontent.com/70241561/121460281-15e28e80-c983-11eb-9b34-c89f83521e7e.png)

prediction with prophet
<p>&nbsp;</p>

![image](https://user-images.githubusercontent.com/70241561/121460306-1e3ac980-c983-11eb-947d-1ba2ff6999ea.png)

Components for the time series. We can see the linear trend. 

<p>&nbsp;</p>

Lastly i used flask to implement both the classificatino model and the prophet model.

![image](https://user-images.githubusercontent.com/70241561/121460474-5a6e2a00-c983-11eb-8752-d010cdf9d5ea.png)



![image](https://user-images.githubusercontent.com/70241561/121460489-62c66500-c983-11eb-9c43-704faf210dd1.png)

Predicted and example for transaction, as well and predicting the revenue in then next 365 days.



