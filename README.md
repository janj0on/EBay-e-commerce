Setup Instructions

Before running this project, you must create an eBay developer account and obtain API credentials.

1. Create an eBay Developer Account

Go to the official eBay Developer Program:
eBay Developers Program

Sign up or log in
Create an application
Generate your API credentials:
Client ID
Client Secret

For security reasons, do NOT hardcode credentials in your code.

Instead, store them as environment variables:

EBAY_CLIENT_ID=your_client_id_here
EBAY_CLIENT_SECRET=your_client_secret_here

You can also use a .env file with python-dotenv.


Output Data

The pipeline generates:

Fact tables
Dimension tables

All outputs must be saved as CSV files.

Saving Data with Pandas

Use pandas to export tables:

fact_table.to_csv("fact_table.csv", index=False)
dim_users.to_csv("dim_users.csv", index=False)
dim_products.to_csv("dim_products.csv", index=False)
