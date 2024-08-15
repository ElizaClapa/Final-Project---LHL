# <p style="text-align: center;"> ⚙️🔍📉 Final Project - 🍞 Bread & Butter Bakery 🧈 Market Basket Analysis 📈🔎🛠️</p>
# <p style="text-align: center;"> ...🥐.....🥧......🍪.....🥖.....🍞.....🥨.....🧁......🎂.....🥯...</p>


## Project Task 🎰🚂

### Recommendation Engine
Perform Market Basket Analysis to create a Recommendation Engine for the Bread & Butter Bakery website, using historical sales transactions information from Bread & Butter Bakery. 


## Dataset
### Shopify - For Recommendation Engine

From Bread & Bakery's Shopify Online Store, the following reports were retrieved:

- Sales by Product
- Sales by Product Variant SKU
- Product Order and Returns
- Payment by Type
- Net Sales

The datasets were combined to create a new table with more transaction details. The new data frame includes the following columns:

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Sale ID</th>
      <th>Date</th>
      <th>Order ID</th>
      <th>Order</th>
      <th>Product</th>
      <th>Net sales</th>
      <th>Payment type</th>
      <th>Credit card</th>
      <th>Credit card type</th>
      <th>Billing country</th>
      <th>Refunds</th>
      <th>Net payments</th>
      <th>returned_item_rate</th>
      <th>product_type</th>
      <th>sales_count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>36</th>
      <td>13091874341004</td>
      <td>2022-06-01T15:01:52-04:00</td>
      <td>4090724483212</td>
      <td>#19196</td>
      <td>coleslaw</td>
      <td>12.5</td>
      <td>Shopify Payments</td>
      <td>Visa</td>
      <td>Standard</td>
      <td>Canada</td>
      <td>0.0</td>
      <td>132.45</td>
      <td>0.0</td>
      <td>Fathers</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>

## Preprocessing and Cleaning Data

1. Product names and product type condensing
2. Handling null values
3. Product type mapping

## Exploratory Analysis and Visualization

## Market Basket Analysis (MBA) - Apriori

For the MBA the dataset was filtered to include only transactions that didn't result in a refund, so the matrix only represents transactions that di not result in refunds/returns. 

A new column with count of products sold per order was also added.

### 1. MBA using Product names.
A MBA was done using the Product names to draw associations. 

The dataset 

### 2. MBA using Product Type names. 
A MBA was done using the Product Types to draw associations. 

## Recommendation Engines

## Deployment 
