

# 👋 Hi, I’m Amr Helmy  
💼 Tax Accountant | 🐍 Python Automation Developer | 📊 Finance & Tax Automation Specialist  

---

## 🚀 About Me
- I work as a **Tax Accountant** with strong knowledge of the Egyptian Tax Law (Law 91 of 2005).  
- I use **Python + Excel** to build automation tools for:  
  - Processing and reconciling tax data  
  - Automating electronic invoice submission  
  - Extracting and analyzing data from files and emails  
- My goal: **Automate repetitive accounting and tax tasks to save time and improve accuracy**  

---

## 🔧 Tools & Technologies
- **Python** (pandas, openpyxl, win32com, requests)  
- **Excel VBA & Formulas**  
- **SQL & Databases** (for data management)  
- **Power BI** (for reporting & analytics)  

---

## 📌 Projects I’ve Worked On
- 🧾 Script for uploading invoices to the Egyptian e-invoicing system  
- 📂 Tool to automatically extract attachments from Outlook emails  
- 📊 Program to reconcile trial balance with financial position statements  
- 🏦 Tax depreciation and corporate tax automation scripts  

---

## 🖥️ Showcase (Practical Examples)

### 🔹 1- Uploading Electronic Invoices
```python
from functions import Get_Token, Post_Document
from openpyxl import load_workbook

# Simple example: Upload invoices from Excel
token = Get_Token()
wb = load_workbook("invoices.xlsx")
sheet = wb.active

for row in sheet.iter_rows(min_row=2, values_only=True):
    invoice = {"id": row[0], "amount": row[1]}
    Post_Document(token, invoice)
