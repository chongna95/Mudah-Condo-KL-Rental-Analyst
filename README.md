# 🏙️ Mudah-Condo-KL-Rental-Analyst
A web scraping tool and dataset generator built with Python for analyzing **Kuala Lumpur condo/apartment rentals** on [Mudah.my](https://www.mudah.my/kuala-lumpur/apartment-condominium-for-rent). This tool helps you collect structured data like property name, area, size (sq.ft), and rental price (MYR) for data analytics purposes.
Afterward, group the data by property name and area, then calculate the average price and average size (sq.ft) for each group, to understand rental trends across different properties and areas.

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
- ✅ Displays real-time **progress bar** using `tqdm`
- ✅ Exports to CSV for further analysis

---

## 📦 Dependencies

Install these via pip if you're running locally:

```bash
pip install requests beautifulsoup4 pandas tqdm
```

---

## 🛠 How It Works

The scraper:

**1.** Starts from page 1 of the KL rental listing page  
**2.** Loops through each listing block  
**3.** Extracts relevant info using `BeautifulSoup`  
**4.** Cleans up fields (removes special characters, parentheses, etc.)  
**5.** Continues until no more listings are found  
**6.** Stores all data into a `pandas.DataFrame` and exports to `CSV`  

---

## 📈 Output Sample

| Property Name | Area       | Average Size (Squared Feet) | Average Rental (MYR) |
|---------------|------------|-----------------------------|----------------------|
| 10 Mont Kiara	| Mont Kiara | 3720.0                      | 14000.0              |
| One KL        | KL City    | 3285.0                      | 14000.0              |  

---

## 📊 Use Cases

- Rental trend analysis by area  
- Price per sq.ft benchmarking  
- Property name & area-based aggregation  
- Dashboard integration (e.g., Tableau, Power BI)  
- Real estate investment insights  

---

## 📁 Output File

- CSV file saved as: `mudah_rental_data.csv`  
- Stored in the same working directory  

---

## 🔗 Run in Colab

👉 [Open Notebook in Google Colab](https://colab.research.google.com/drive/1pXJ-3Cjf0Gy05Nbd-pj0_p0ilvblEJ_w#scrollTo=S3-0ELgXvUsr)

---

## 🧼 Notes

- Scraper skips listings without size or price.  
- Automatically removes values inside brackets (e.g. `Block 15,17`).  
- Replaces missing values with `None`.  






