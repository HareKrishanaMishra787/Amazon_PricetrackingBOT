# 🔔 Amazon Price Tracker 🛒

A Python-based **Amazon Price Tracker** that sends you an **email alert** when a product’s price drops below your target. Perfect for getting the best deals without constantly checking manually!

---

## 🧠 What It Does

- 🕵️ Scrapes product price and title from Amazon
- 🔁 Checks if the current price is below your set threshold
- 📧 Sends you an **email alert** when the item is on sale
- 🌐 Works on any Amazon product page (just replace the URL!)

---

## 🚀 How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/amazon-price-tracker.git
cd amazon-price-tracker
```

### 2. Install Dependencies
```bash
pip install requests beautifulsoup4 python-dotenv
```

### 3. Configure Environment Variables

Create a `.env` file in your project directory with the following:
```
MY_SMTP_ADDRESS=smtp.gmail.com
MY_EMAIL=your_email@gmail.com
MY_PASSWORD=your_email_app_password
```

✅ Use an **App Password** for Gmail (if you have 2FA enabled).

---

## ✍️ Modify Your Target Product

Edit the `url` in `main.py` to point to your desired Amazon product:
```python
url = "https://www.amazon.in/dp/B01LYEV6RF"
```

Also adjust your desired price:
```python
BUY_PRICE = 400
```

---

## ▶️ Run the Script
```bash
python main.py
```

If the product is under your `BUY_PRICE`, you'll get an email like:

```
Subject: Amazon Price Alert!
Body: Apple AirPods Pro is on sale for ₹399! 
```

---

## 🛠 Troubleshooting

- **Price not found?** Amazon's HTML can change—inspect the page and update the scraping logic if needed.
- **Email not sending?** Check SMTP config, or ensure less secure apps are allowed (or use an app password).

---

## 💡 Tip

You can set this up to run on a schedule using:
- `cron` on Linux/macOS
- Task Scheduler on Windows
- Python's `schedule` library for a script-based timer

---

## 🙏 Credits

- Uses [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/) for parsing HTML
- Thanks to [Amazon](https://www.amazon.in/) for the product listings

---

## 🌟 Like This Project?

Star the repo ⭐ and share it if it helped you grab a deal!
