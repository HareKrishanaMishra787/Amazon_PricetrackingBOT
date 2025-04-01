# Amazon_PricetrackingBOT is an Amazon Price Tracker that monitors the price of a product on Amazon and sends an email notification when the price drops below a set threshold.

Project Overview
This script scrapes an Amazon product page to check its current price and sends an email alert if the price falls below a predefined value.

How It Works
Web Scraping:

Uses requests and BeautifulSoup to fetch and parse the product page.

Extracts the product title and price.

Price Comparison:

Converts the extracted price into a numerical format.

Compares it with a predefined "BUY_PRICE."

Email Notification:

Uses smtplib to send an email alert when the price drops.

Retrieves email credentials from an .env file using dotenv.

Requirements
requests for HTTP requests.

BeautifulSoup for HTML parsing.

smtplib for sending emails.

dotenv for environment variable management.
