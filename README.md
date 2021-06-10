# Google-Analytics
Clustering, Time Series and Classification on a sample from a Google Analytics Dataset




This Project is based on a sample of a dataset from a google analytics gathering. The objectives of this project were multiple.\
First i analysed the data and make some charts that better represent this daatset.\
Then i did some clsutering to group clients and analyse the groups a bit.\
After that i did some classification. I tried to predict whether the client would or would not make a transaction.\
Then i did some time series prediction on the revenue.\
Lastly i used flask to implement both the time series model as well as the classification model, giving a full report.



<img align="left"  width="250" height="250" src="https://user-images.githubusercontent.com/70241561/121459170-23971480-c981-11eb-8d21-0a9a20ba9b36.png"> 



The percentage of nulls was great. I had to drop a lot of columns due to nulls or not giving any information. Also used some imputation techniques. The balance of classes for the classification was 98% for one class and 2% for the other, Instead of using undersampling or oversampling, I trained the model with the real data, use AUC and F1 Score as metrics to compare models and move the threshold. The percentage of classes was so great, if i used some some of sample alteration then i would have changed the data too much.




<p>&nbsp;</p> 
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
