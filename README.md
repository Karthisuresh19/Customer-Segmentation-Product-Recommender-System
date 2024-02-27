This project aims to analyze customer behavior and preferences through segmentation based on recency, frequency, and monetary values (RFM), as well as to provide personalized product recommendations using cosine similarity.

Table of Contents
Introduction
Features
Customer Segmentation
Product Recommender System
Usage
Dependencies


Introduction
Understanding customer behavior and preferences is crucial for businesses to tailor their marketing strategies and enhance customer satisfaction. This project employs RFM analysis to segment customers based on their transaction history and subsequently builds a product recommender system to suggest relevant products to users.

Features
RFM Analysis: Segmentation of customers based on recency, frequency, and monetary values of their purchases.
Product Recommender System: Utilizes cosine similarity to identify relevant unbought products for a user.


Customer Segmentation
Customer segmentation is performed using the RFM model, which categorizes customers based on the following criteria:
Recency: How recently a customer has made a purchase.
Frequency: How often a customer makes purchases.
Monetary: The total amount of money a customer has spent.
By analyzing these factors, customers are segmented into distinct groups, allowing businesses to target their marketing efforts more effectively.

Product Recommender System
The product recommender system utilizes cosine similarity to identify similar users and with that, products that are not yet pruchased by a user but bought by the user's similar users are recommended to a user. The process involves the following steps:

Calculate the cosine similarity between the users' purchase history
Note the users with the highest cosine similarity scores to our user.
With the noted similar users purchase information, we can recommend products to our user accordingly

Usage
To use the customer segmentation and product recommender system:

Ensure that the necessary data (customer transaction history, product inventory) is available.
Run the segmentation algorithm to categorize customers based on RFM values.
Implement the product recommender system to generate personalized recommendations for users.

Dependencies
The project relies on the following dependencies:

numpy
pandas
scikit-learn
Ensure that these dependencies are installed to successfully run the project.
