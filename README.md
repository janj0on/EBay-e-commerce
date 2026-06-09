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

Environment Variables

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

Make sure:

index=False is used to avoid saving row indices
Files are stored in a clear directory structure if needed (e.g. /data/)

Suggested Project Structure
project/
│
├── data/
│   ├── fact_table.csv
│   ├── dim_users.csv
│   └── dim_products.csv
│
├── src/
│   ├── extract.py
│   ├── transform.py
│   └── load.py
│
├── .env
├── requirements.txt
└── README.md
 Requirements

Notes
Keep your API credentials private.
Do not push .env files to GitHub.
Always regenerate credentials if they are exposed.
