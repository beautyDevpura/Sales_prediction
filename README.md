Hello,
This is the project about sales prediction using different Machine learning algorithms. Also various Data visualization methods used for graphical representation.
For this project I used data of Big mart Shopping centre.
In the Dataframe 1463 values missing  in column  Item Weight and 2410 values missing in column Outlet Size out of total 8522 rows and 12 columns
Instead of dropping such a large number of data, replacing Nan values with some other value is wise. I used INTERPOLATE method to replace missing values of Item Weight column which is a numeric column. I also used PAD method for missing values in Outlet_Size column which is an object column
Also, managed String Inconsistency for column Item Fat Content. 
![salesproject3 (1)](https://user-images.githubusercontent.com/82862957/120975917-a708f980-c726-11eb-8052-acd0d5e820d5.png)
![salesproject4](https://user-images.githubusercontent.com/82862957/120976362-1ed72400-c727-11eb-8442-91a9535c8859.png)
In 1998, only Grocery stores were established and notice, that year has the least Average Sale. what does this indicate is Sales value is not impacted by how old the particular outlet is!
![salesproject5 (1)](https://user-images.githubusercontent.com/82862957/120976296-0e26ae00-c727-11eb-9d48-10d6e7f45199.png)
In year 1985, one Outlet OUT27 which has Supermarket type 3 was established.
Grocery store opened in 1985 and 1998, SuperMarket Type 1 opened in 1987, 1997, 1999, 2002, 2004, 2007 and Supermarkete Type 2 was 2009 and as mentioned earlier Type 3 was opened in 1985.
Only one Outlet has a Supermarket Type 3 - OUT27. OUT27 has a highest contribution in Average Sale as per Outlet Type.
![salesproject7](https://user-images.githubusercontent.com/82862957/120976566-4e862c00-c727-11eb-9dac-952cd3f5fa4b.png)

Fruits and Vegetable & Snack Foods have highest sales Revenue. Also consumer prefer more Low Fat content products over Regular Fat content products.
OneHotEncoder method has been used to deal with Object columns. So that these Categorical columns can be useful in Sales prediction Model.
List of columns converted to Binary: Item_Fat_Content, Item_Type, Outlet_Type, Outlet_Establishment_Year, Outlet_Size and Outlet_Location_Type 
Independent feature columns are all columns except Item_Identifier, Outlet_Identifier and dependent Column is Item_Outlet_Sales
Train_test_split method has been used to split into Test data and Train data.Train Data will be useful to train the Machine Learning models while Test Data will be used to check the score of the models.  

>Feature Importance using Random forest method< 
![salesproject10](https://user-images.githubusercontent.com/82862957/120976846-9311c780-c727-11eb-826a-7ab5e7e564f6.png)

>Correlation between OUTLET TYPE and ITEM OUTLET SALES<
![salesproject15](https://user-images.githubusercontent.com/82862957/120977148-df5d0780-c727-11eb-8b60-a0507c7e21f7.png)
Above graph indicates the Type of OUTLET really affects the and contributes in large number in OUTLET SALES

Linear Regression Model: 
Score with Train Data: 0.5550005285787925 
Score with Test Data: 0.588649515596599

KNN model: 
Score with train data: 0.6031768916686765 
Score with test Data: 0.45610930332602073

Random Forest Model: 
Score with Train data: 0.6177702641715458 
Score with Test data: 0.6204671735370194
Random Forest Model is giving best score out all. It is even performing better in Test data. 0.62 is best score retrieved after trying multiple parameters tuning for Random forest model.
![salesproject9](https://user-images.githubusercontent.com/82862957/120979094-13392c80-c72a-11eb-9598-9d7538656ab6.png)

For Features significance and their impact on Sales, Its found from analysis that Item MRP has Highest impact and contribution on Total Sales but its not advise to increase the Item price which can impact negative in future. Instead Other areas should be more focused like, OUTLET TYPE and ITEM TYPE have very high impact on Sales.
Grocery Stores have negative Correlation with Sales, so upgrading Grocery Stores to Type 1 or bigger Type can really impact the sales in great manner.
Fruits and Vegetable, Snack foods, Dairy, HouseHold items have high impact on Sales. So these product should be focused more than Health and Hygiene and Soft Drinks Items. 
Other Features have negligible impact on Sales. 


