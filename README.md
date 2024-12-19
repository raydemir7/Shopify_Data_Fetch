# Shopify Data Fetch and Reporting via API

This script automates fetching order data from a Shopify store via the Shopify Admin API, processes key metrics like sales, refunds, and taxes, and writes the results to Google Sheets. The script supports daily data breakdowns, handles API rate limits, and ensures all dates within the specified range are filled.

Shopify can be very challenging fetching the correct values, u need to analyse all metrics very carefully.

## Features
- Fetches Shopify order data for a specified date range.
- Aggregates metrics including:
  - **Subtotal** (Total order value before taxes and shipping)
  - **Tax**
  - **Shipping**
  - **Refunds**
  - **Total Sales**
  - **Order Count**
- Handles missing dates in Google Sheets and appends new data.
- Automatically updates the latest data for today and yesterday.
- Handles rate limits and server errors with retry logic.

## Technologies Used
- **Python**: For scripting and processing data.
- **Shopify Admin API**: For fetching order data.
- **Google Sheets API (gspread)**: To write reports in Google Sheets.
- **Google Cloud Functions**: To automate the script execution via Pub/Sub.

---

## Prerequisites

### Shopify API Credentials
1. Access your Shopify Admin API settings.
2. Generate an API key, API secret, and access token.
3. Set the following environment variables:
   - `SHOP_API_KEY`: Your Shopify API Key.
   - `SHOP_API_SECRET`: Your Shopify API Secret.
   - `SHOP_API_TOKEN`: Your Shopify Access Token.

### Google Sheets API Credentials


### Python and Required Packages
- Python 3.9+
