# Data Science Project
The projects in this repository are part pf my academic project done during my diploma degree in Data Science.
> Please edit the dataset name according to the project notebook the name written in the `pd.read_csv` code after clonning present in the Dataset folder.

#### 1. [Uber Assignment](https://github.com/snozh5/Data-Science-Project/blob/main/Uber%20Assignment.ipynb)
<b>Problem Statement:</b> The aim of analysis is to identify the root cause of the problem (i.e. cancellation and non-availability of cars) and 
recommend ways to improve the situation. As a result of the analysis, one should be able to present to the client the root cause(s) and possible 
hypotheses of the problem(s) and recommend ways to improve them.
<br>
<br>
<b>Solution:</b>
<p align="left">
  <img src="Image/UberPickupPoint.png" width="200">
  <img src="Image/UberSuppyGapTimeslot.png" width="200">
</p>

The above bubble plot shows the most pressing problem for Uber is No Cars Available at the Airport and the time is mostly evening hour from the bar graph we can conclude.

Some of the ways to resolve the issue:-
- Increase the number of cars available the customers.
- Increase the radius of the map for the app during the pick hour i.e. evening in the airport.
- Communication should be done with the driver so that they can be available at airport during the evening timeslot and make themselves available.

#### 2. [Car Price Prediction Assignment](https://github.com/snozh5/Data-Science-Project/blob/main/Assignment-%20Linear%20Regression%20(Geely%20Auto).ipynb)
<b>Problem Statement:</b> The aim of this project is to model the price of the cars which will be used by the management to understand the important KPIs and pricing dynamics of the market.

<b>Solution:</b> For this project since the target variable price is continuous a Linear Regression Model is being trained to find out the important KPIs impacting the price. The matrix used to evaluate the model is R-squared value and for building the model I have used the following technique:
<br>
![Structure](https://github.com/snozh5/Data-Science-Project/blob/main/Image/Linear%20Regression%20Structure.png?raw=true)

<p align="left">
  <img src="Image/Car Price Company name.png" width="400">
</p>
The above plot shows the Company name of different cars in the dataset.<br>
The final result of the model achieved a final R-square value of 88% which means the model the will do a decent good job and be able to find out the important KPIs. So after iteration, the final features left are:-

- Porsche (Company Name)
- Rear (Engine Location)
- Curbweigt
- Peugeot (Company Name)
- BMW (Company Name)
- Twelve (Cylinder Number)

These are the important KPIs that are impacting the price of the car and hence the management can use to determine the pricing dynamics of the market. 

#### 3. [House Price Prediction Assignment](https://github.com/snozh5/Data-Science-Project/blob/main/Advanced%20Regression.ipynb)
<b>Problem Statement:</b> The aim of this project is to find out the important variables that affect the price of the house and how those variables describe the price of the house.
<br>
<br>
<b>Solution:</b> For this project I have used Ridge and Lasso algorithm which are also known as Advance Regression. What it does is they give us important features after the model is being trained.<br>
A cross-validation GridSearchCV equal to 10 is used to determine the alpha value. For Ridge Regression alpha equal to 10 came out as best value and for Lasso an alpha vlue of 100.

<p align="left">
  <img src="Image/House imp var.png" width="300">
</p>
The above plot shows the end result of important features for the Lasso model.

#### 3. [Clustering Countries based on Socio-economic Conditions](https://github.com/snozh5/Data-Science-Project/blob/main/Clustering%20and%20PCA%20.ipynb)
<b>Problem Statement:</b> HELP International is an international humanitarian NGO that is committed to fighting poverty and 
providing the backward countries with the basic amenities. The job is to categories the countries using socio-economic 
and health factors that determines the overall development of the country. To achieve that the countries are clustered by 
the factors mentioned in the data and then present the solution and recommendation on which countries should be given more 
preference and look-after for help financially.

> Outliers are not treated based on the business objective it was assumed that outliers won't affect much on the outcome. <br>

<b>Solution:</b>It's clear that is an unsupervised learning project so to cluster the countriues based on the given features K-means technique is used with different clusters also Heirarchical Clustering is being used for double check the result. Dimensionality reduction technique i.e. Priciple Component Analysis (PCA) is used in this project for the input features. 

![PCA](https://github.com/snozh5/Data-Science-Project/blob/main/Image/variance%20(PCA).png)

The above plot is the screeplot to access the number of Principle Componet needed in order to gain.attain maximum variance. From the graph we observe that at 95% variance can be captured using five PCs.

![SSD](https://github.com/snozh5/Data-Science-Project/blob/main/Image/SSD.png)

The above plot is a sum of square distance curve is plotted showing similar results, a point from 3 to 5 looks good for clustering K-Means.<br>

***K-Means Clustering*** <br>
1. K value as 5
<img src="https://github.com/snozh5/Data-Science-Project/blob/main/Image/PCA_country_k5.png" width="500">

The above plot shows the top 20 countires when the value of K is 5.

2. K value as 4
<img src="https://github.com/snozh5/Data-Science-Project/blob/main/Image/PCA_country_k4.png" width="500">

The above plot shows the top 20 countires when the value of K is 4.

3. K value as 3
<img src="https://github.com/snozh5/Data-Science-Project/blob/main/Image/PCA_country_k3.png" width="500">

The above plot shows the top 20 countires when the value of K is 3.
<br>
Common countries all the three clusters are: Burundi, Liberia, Congo, Dem. Rep., Niger, Sierra Leone, Madagascar, Mozambique, Central African Republic, Malawi, Eritrea, Togo, Guinea-Bissau, Afghanistan, Gambia, Rwanda, Burkina Faso ,Uganda, Guinea , Haiti ,Tanzania, Nepal, Tajikistan , Bangladesh, Cambodia, Kyrgyz Republic, Myanmar, Solomon Islands, Vietnam, India, Uzbekistan, Moldova, Bolivia, Philippines, Bhutan, Egypt, Mongolia, Sri Lanka, Guatemala, Morocco, Micronesia, Fed. Sts.

***Hierarchical Clustering*** <br>
<img src="https://github.com/snozh5/Data-Science-Project/blob/main/Image/country.png" width=500>

For the Hierarchical clustering a dendogram is created using complete method. Further dendogram is cut into 3 clusters to form the cluster of country. Nothing much insights was formed after creating the clusters using Hierarchical clustering using PCs. The only country that influenced the most was Nigeria from cluster 2 followed by Luxembourg, Malta, Seychelles, Singapore. <br>
***Conclusion:*** The analysis is done using both K-Means & Hierarchical Clustering and based on the visualization and the outcome, K-Means should be preferred using three as a value of K. 
