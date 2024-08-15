# <p style="text-align: center;"> 🍞 Bread & Butter Bakery 🧈 Market Basket Analysis </p>

## Project Task 🎯🚀

### Recommendation Engine 🛒🤖
The goal of this project is to perform Market Basket Analysis to create a Recommendation Engine for the Bread & Butter Bakery website, using historical sales transaction information. The engine is expected to enhance the customer experience by recommending products based on their purchasing behavior, ultimately increasing cross-sell and up-sell opportunities.

**Demonstration video ▶️:**
[![Deployment video](https://github.com/ElizaClapa/Final-Project---LHL/blob/main/Data/4.%20Deployment/Deployment%20Picture.png?raw=true)](https://youtu.be/2eHn0dAzdfM)

## Dataset 📊

### Shopify - For Recommendation Engine 🛍️💻
From Bread & Butter Bakery's Shopify Online Store, the following reports were retrieved:

- Sales by Product 📈
- Sales by Product Variant SKU 🔢
- Product Order and Returns 🔄
- Payment by Type 💳
- Net Sales 💰

These datasets were combined to create a detailed transaction table. The resulting DataFrame includes columns such as `Sale ID`, `Date`, `Order ID`, `Product`, `Net sales`, `Payment type`, `Billing country`, `Refunds`, `Net payments`, and more.

## Preprocessing and Cleaning Data 🧼🛠️

1. **Product Name and Type Condensing**: Product names and types were condensed to standardize the data for analysis.
2. **Handling Null Values**: Null values were handled appropriately to ensure the data's integrity.
3. **Product Type Mapping**: Products were mapped to their respective types for higher-level analysis.

## Exploratory Data Analysis (EDA) 🔍📊

The EDA phase uncovered several key insights:
- **Sales Trends** 📅📈: Identified peak sales periods and popular products.
- **Customer Behavior** 🛒📊: Patterns in customer purchases highlighted the most frequently bought items and the types of products that tend to be bought together.

## Market Basket Analysis (MBA) - Apriori 🧺🛒

For the MBA, the dataset was filtered to include only transactions that did not result in refunds. The analysis was performed at two levels:

### 1. MBA using Product Names 🏷️
- Associations between individual products were analyzed.
- **Key Findings** 💡: The updated network graph provides an intricate look at associations between individual products from Bread & Butter Bakery's online store, highlighting the specific items that are frequently purchased together. The strength of these associations is visualized through the thickness and color intensity of the edges connecting the products, with the "Lift" metric serving as a key indicator of how much more likely two products are to be bought together compared to what would be expected by chance.

	1. **Strong Product Associations** 💪:
    	- **Apple Pie and 9-Inch Pumpkin Pie** 🥧: The network shows a strong connection between "Apple Pie" and "9-Inch Pumpkin Pie," evidenced by a significant lift value of 5.42. This association suggests that these pies are frequently purchased together, particularly during holiday seasons, making them prime candidates for cross-promotion in seasonal bundles.
    	- **Assorted Holiday Cookies and Scottish Shortbread** 🍪: Another notable pairing is between "Assorted Holiday Cookies" and "Scottish Shortbread," with a high lift value of 10.81. This strong association is ideal for holiday promotions, where both items could be bundled together to drive sales during festive periods.

	2. **Prominent Products** 🌟:
    	- **Apple Pie** 🍏: Serving as a central node in the graph, "Apple Pie" is highly connected to several other products, including "9-Inch Pumpkin Pie," "Blueberry Pie," "Raspberry Pie," and "12 Dinner Rolls." This indicates that "Apple Pie" plays a pivotal role in driving the purchase of related products, making it a critical item for upselling and cross-promotional strategies.
    	- **12 Dinner Rolls** 🥖: This product also holds a central position in the network, with strong associations to various pie types. The prominence of "12 Dinner Rolls" suggests that it could be effectively marketed as part of meal deals or family-sized bundles, catering to customers seeking convenient and comprehensive meal options.

	3. **Opportunities for Cross-Promotion** 🔄:
   	 	- **Platter Associations** 🥪🍇: The connections between "Sandwich Platter," "Crudité Platter," and "Fruit Platter" indicate that customers who purchase one platter are likely to buy another. This presents an opportunity to offer special deals on catering packages or party bundles, which could include combinations of these platters.
   	 	- **Pie Combinations** 🥧🥧: The strong ties between various pie types, such as "Apple Pie," "9-Inch Pumpkin Pie," and "Blueberry Pie," suggest a customer preference for variety. This could be leveraged by offering mix-and-match pie deals or discounts on multiple pie purchases.

	4. **Product Isolation** 🚶‍♂️:
   		 - **Fruit Platter** 🍓: The "Fruit Platter" is relatively isolated in the network, indicating that it is not frequently purchased alongside other items. To enhance its visibility and sales, it could be bundled with more popular items like the "Crudité Platter" or highlighted in promotional campaigns targeting health-conscious customers.

	5. **Edge Strength and Interpretation** 🕸️:
		- The thickness and color intensity of the edges in the graph clearly indicate the strength of the associations between products. The most intense and thickest edges represent the strongest associations, making it easy to identify key product pairings that should be the focus of promotional efforts.

![Market Basket Analysis Results 1](https://github.com/ElizaClapa/Final-Project---LHL/blob/main/Plots/Basket%20Market%20Analysis%20Results%201.png?raw=true)

- **Implications for Business Strategy** 📈:

	- **Promotion and Cross-Selling** 📢:
    	- The strong associations, such as between "Apple Pie" and "9-Inch Pumpkin Pie," as well as between "Assorted Holiday Cookies" and "Scottish Shortbread," suggest excellent opportunities for targeted promotions. Seasonal bundles featuring these pairings could be particularly effective.
    	- Additionally, promoting platter combinations, like the "Sandwich Platter" and "Crudité Platter," could attract customers looking for catering options, further boosting sales.

	- **Inventory Management** 📦:
    	- Given the strong connections between certain products, it will be important to ensure that sufficient inventory is maintained, especially during peak seasons. For example, keeping ample stock of both "Apple Pie" and "12 Dinner Rolls" will be crucial, as these items are often purchased together.

	- **Customer Experience** 🤝:
    	- By strategically placing frequently associated products near each other on the online store, the shopping experience can be optimized. This approach not only makes it easier for customers to find and purchase related items but also has the potential to increase the average transaction value.

- **Conclusion** 📝:

	The enhanced product-level Market Basket Analysis offers actionable insights into customer purchasing behavior at Bread & Butter Bakery's online store. By focusing on specific product pairings and leveraging these insights for strategic promotions and inventory management, the bakery can improve its online sales performance and better meet the needs of its customers. The updated network graph, with its emphasis on edge strength and color intensity, provides a clear visual guide to the most promising opportunities for cross-promotion and product bundling.


### 2. MBA using Product Types 📦
- A broader analysis was conducted using product types.
- **Key Insight** 💡: The network graph displayed above visualizes the association rules derived from a Market Basket Analysis of Bread & Butter Bakery’s online store. This analysis reveals patterns in customer purchasing behavior, identifying which product types are frequently bought together. The strength of these associations is quantified using the "Lift" metric, represented by the thickness and color intensity of the edges in the graph. The graph provides actionable insights into how different product types interact within the online store, informing strategic decisions for marketing, inventory management, and customer experience optimization.

	1. **Strong Associations** 💪:
    	- **Bread and Savoury** 🥖🍲: This pairing exhibits a strong association, as indicated by the prominent edge connecting these nodes. The significant lift suggests that customers who purchase bread are also very likely to buy savory items, making this combination ideal for online bundle deals or meal promotions.
    	- **Bread and Cookies** 🥖🍪: The connection between bread and cookies is another robust association highlighted by the network. This relationship indicates that these items are often purchased together, presenting opportunities for cross-promotion, particularly in the form of “breakfast packs” or “snack bundles” in the online store.
    	- **Cakes and Bread** 🍰🥖: Another notable connection is between cakes and bread, underscoring the importance of these staple items in driving complementary sales. Given their popularity, these items could be featured in online promotions to enhance average transaction values.

	2. **Product Type Combinations** 🔄:
    	- The network includes nodes representing combinations of product types, such as "bread, cookies" and "cakes, savoury." These nodes illustrate scenarios where customers purchase multiple types of items in a single transaction. The combinations reflect common customer preferences in the online shopping environment, offering insights into potential multi-item offers or discounts that can be promoted online.

	3. **Product Type Importance** 🌟:
    	- **Bread** 🥖 emerges as a central node in the network, connecting to multiple product types like cakes, cookies, and savory items. This centrality highlights bread as a crucial driver of online sales for other products, making it a key focus for cross-selling strategies and ensuring sufficient online inventory.
    	- **Savoury Items** 🥧🍲 are also integral to the network, frequently associated with other baked goods like bread and cakes. This indicates that customers tend to purchase savory items alongside sweet options, which could be leveraged in meal deals or combo offers available exclusively online.

	4. **Edge Strength and Interpretation** 🕸️:
    	- The edges connecting the nodes vary in thickness and color intensity, correlating with the lift values. Stronger associations are represented by thicker, darker edges, providing a clear visual indication of which product pairings are most significant. This visualization aids in identifying the most impactful associations for online marketing and inventory decisions.
    	- The color bar on the right serves as a key to interpreting the strength of associations, with brighter colors indicating stronger associations. This allows for a quick assessment of which product combinations are most relevant for enhancing sales through the online platform.

![Market Basket Analysis Results 3](https://github.com/ElizaClapa/Final-Project---LHL/blob/main/Plots/Basket%20Market%20Analysis%20Results%203.png?raw=true)

- **Implications for Business Strategy** 📈:
	- **Promotion and Cross-Selling** 📢:
    	- The strong associations, such as between "Bread and Savoury" or "Bread and Cookies," highlight opportunities for cross-selling and bundling in the online store. For instance, offering a discount when customers purchase bread along with cookies or savory items could increase the average transaction value.
    	- Bundled promotions that reflect common customer purchasing patterns, like a "Bread and Savoury Combo" or a "Cake and Savoury Meal Deal," could be prominently featured on the online store to encourage higher sales.

	- **Inventory Management** 📦:
    	- Recognizing these associations enables more precise demand forecasting for online sales. For example, an increase in bread sales could signal a likely rise in demand for savory items, allowing the bakery to prepare and stock accordingly.
    	- Maintaining sufficient online inventory levels of strongly associated products can help avoid stockouts and capitalize on the natural co-purchasing behaviors of customers, particularly during peak shopping periods or promotional events.

	- **Customer Experience** 🤝:
    	- The online store layout can be optimized to place strongly associated products in close proximity within the digital interface, making it easier for customers to find and purchase related items. This could enhance the customer shopping experience and potentially increase the overall sales volume.
    	- Implementing an online recommendation system that suggests related products based on these associations could further improve the customer journey, driving higher engagement and conversion rates.

- **Conclusion** 📝

	The association rules network graph provides critical insights into the online purchasing behavior of customers at Bread & Butter Bakery. By understanding these associations, the bakery can refine its online marketing strategies, optimize inventory management, and enhance the online shopping experience, ultimately driving sales growth and increasing customer satisfaction.

## Recommendation Engine 🤖💡

Based on the MBA results, a recommendation engine was developed. The engine recommends products based on the contents of the customer's shopping cart, aiming to increase the average order value.

### Expected Impact on Sales 💸📈
- **Increased Cross-Sell Opportunities** 🎯: By recommending related products, the engine encourages customers to purchase additional items.
- **Enhanced Customer Experience** 🌟: The tailored recommendations create a more personalized shopping experience, increasing customer satisfaction and retention.

### How the Recommendation Engine Works 🤖

The recommendation engine for Bread & Butter Bakery leverages Market Basket Analysis (MBA) to generate personalized product recommendations based on historical sales data. The engine operates at both the **product level** and **product type level** and also considers the **sales count** to suggest the most relevant items to customers.

#### Key Steps 🗝️:

1. **Preprocessing Input Products** 🔄:
   - Product names are standardized by converting them to lowercase and removing special characters. This ensures consistency when matching products against association rules.

2. **Matching Association Rules** 🕵️‍♂️:
   - **Product-Level Associations** 🛒: The engine first attempts to find recommendations by matching the exact products in the customer's cart with product-level association rules.
   - **Product Type-Level Associations** 📦: If no direct product-level matches are found, the engine falls back on product type associations, grouping products into broader categories to identify patterns.

3. **Generating Recommendations** 🎯:
   - When a match is found at either the product or product type level, the engine recommends items with the highest lift and confidence values, ensuring that the suggested products are the most likely to be purchased together with the items in the customer's cart.

4. **Fallback to Popular Products** 🌟:
   - If no relevant associations are found, the engine recommends the most popular products either across all categories or within the same product type. Popularity is determined based on the sales count from recent transactions, emphasizing items frequently bought during the current period.

5. **Combination of Techniques** ⚙️:
   - The engine intelligently combines association rule mining (using frozensets for matching antecedents and consequents) with sales data analysis to provide a robust recommendation system. This hybrid approach maximizes the relevance of suggestions, increasing the likelihood of cross-sell and up-sell opportunities.

#### Example Workflow 🧑‍💻:

1. **Input**: The customer adds "Buttertarts" to their cart.
2. **Product-Level Search** 🛒: The engine looks for product-level rules matching "Buttertarts".
3. **Fallback to Product Type** 📦: If no direct match is found, it checks for rules based on the product type, such as "Pastries".
4. **Final Recommendations** 🎯: The engine either suggests associated products with high lift and confidence or falls back to recommending the most popular items within "Pastries".

This recommendation system is designed to enhance the customer experience by delivering relevant suggestions, ultimately increasing the bakery’s sales through effective cross-selling and up-selling strategies.

## Deployment 🚀💻

The recommendation engine was deployed using Flask, integrated into a website designed to visually align with the Bread & Butter Bakery brand. The deployment process included:
- **UI Design** 🎨: The Flask app was styled to match the bakery's website.
- **Functionality Testing** 🧪✅: Extensive testing ensured the engine provides accurate recommendations based on various cart contents.

### Deployment Decision Summary 🚀

The recommendation engine for Bread & Butter Bakery was deployed locally using Flask instead of being directly integrated into the Shopify website. This decision was made for the following reasons:

1. **Permissions and Integration** 🔐: Deploying directly to the Shopify website requires specific permissions and API integrations that involve discussions with the bakery's owner. At the time of this project, those permissions had not yet been secured.

2. **Testing and Refinement** 🧪: Local deployment allowed for thorough testing and refinement of the recommendation engine in a controlled environment. This ensures that when the system is eventually integrated into the live Shopify site, it will be stable and effective.

### Future Integration 🔄

In the future, once the necessary permissions are obtained and the owner of Bread & Butter Bakery approves the deployment, the recommendation engine can be integrated into the Shopify website by:

1. **API Integration** 🔗: Utilizing Shopify's API, the recommendation engine can be connected to the live store, dynamically generating product suggestions based on real-time customer behavior.

2. **Shopify App Development** 🛠️: A custom Shopify app can be developed to incorporate the recommendation engine directly into the store’s interface. This app would provide an interface for the engine to interact with the store’s product catalog and customer data.

3. **Owner Collaboration** 🤝: Close collaboration with the bakery’s owner will be essential to ensure the recommendations align with the store’s marketing and sales strategies, maximizing the impact on sales.

This approach ensures that when the recommendation engine goes live on the Shopify website, it will be fully integrated, user-friendly, and aligned with Bread & Butter Bakery's business goals.

### Deployment Links 🔗
https://youtu.be/2eHn0dAzdfM 
