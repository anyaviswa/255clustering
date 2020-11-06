# 255clustering
A detailed analysis on the Instacart Market Basket data to get insights for the targeted marketing and the product recommendation to the customers using the data mining technique, Clustering.

<h3 id="dataset"> Dataset </h3>

The instacart dataset can be downloaded from <a href="https://www.instacart.com/datasets/grocery-shopping-2017">here</a>.

#### orders.csv : 
This file tells to which set (prior, train, test) an order belongs. You are predicting reordered items only for the test set orders. 'order_dow' is the day of week -  order_id,user_id,eval_set,order_number,order_dow,order_hour_of_day,days_since_prior_order.

#### aisles.csv : 
Stores asile details - aisle_id,aisle

#### products.csv : 
Stores product details - product_id,product_name,aisle_id,department_id

#### order_products__*.csv : 
These files specify which products were purchased in each order. order_products__prior.csv contains previous order contents for all customers. 'reordered' indicates that the customer has a previous order that contains the product. Note that some orders will have no reordered items - order_id,product_id,add_to_cart_order,reordered

### Clustering
There are two clustering notebooks.
<ol>
  <li><a href="Clustering-Complete-Analysis.ipynb">Clustering-Complete-Analysis</a></li>
  <li><a href="Clustering-with%20Sample%20Data.ipynb">Clustering-with Sample Data</a>. (approximate execution time: 2 minutes)</li>
</ol>
<h3><a href="Clustering-Complete-Analysis.ipynb">Clustering-Complete-Analysis </a></h3>
This explains the entire process followed in clustering Instacart users.  <br> <br>

<b> Files needed: </b> <br>

The below mentioned files are needed which can be downloaded from <a href="https://www.instacart.com/datasets/grocery-shopping-2017">here</a> and the description of files are provided under <a href="#dataset">dataset section</a>. 
<ol>
  <li>orders.csv</li>
  <li>order_products__prior.csv</li>
  <li>order_products__train.csv</li>
  <li>products.csv</li>
  <li>aisles.csv</li>
</ol>  

<h3><a href="Clustering-with%20Sample%20Data.ipynb">Clustering-with Sample Data </a></h3>
<b>Execution time:</b> 2 minutes <br>
This notebook gives an overview of the clustering process using Sample Data of size (42000,66) extracted from the dataframe of size (206034,130). <br><br>

<b> Files needed: </b> <br>

#### cust_orders.gz
This can be downloaded from <a href="data/cust_orders.gz">here.</a> <br>
This file is the sampled dataset of size (42000,66). It encloses user id and aisles as columns and the rows corresponds to the users. <br><br>

### Clustering output
#### cluster_output.gz
This can be downloaded from <a href="data/cluster_output.gz">here.</a> <br>
This file encloses the <b>clustering output</b> of Instacart users to perform further analysis.
<br><br>

<h3><a href="Clustering-UseCase.ipynb"> UseCase </a></h3>
This Notebook showcases the usecase based on Clustering performed on Instacart dataset.

When an aisle name is given, it displays the list of user id's who are the frequent buyers of that particular aisle's products.
