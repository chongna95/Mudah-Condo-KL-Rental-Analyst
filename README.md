# 🏙️ Mudah-Condo-KL-Rental-Analyst
A web scraping tool and dataset generator built with Python for analyzing **Kuala Lumpur condo/apartment rentals** on [Mudah.my](https://www.mudah.my/). This tool helps you collect structured data like property name, area, size (sq.ft), and rental price (MYR) for data analytics purposes.

---

## 🚀 Features

- ✅ Scrapes **all listing pages**
- ✅ Extracts:
  - Property Name (cleaned of extra symbols and brackets)
  - Area
  - Size in `sq.ft`
  - Rental in MYR
- ✅ Cleans text with regex
- ✅ Handles missing/null fields
- ✅ Displays real-time progress bar using `tqdm`
- ✅ Exports to CSV for further analysis

---

## 📦 Dependencies

Install these via pip if you're running locally:

```bash
pip install requests beautifulsoup4 pandas tqdm
