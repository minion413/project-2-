# Superstore Sales Data Analysis Web App

## Overview
This project is an **interactive web application** built using **Flask** and **Pandas** that allows users to explore and analyze Superstore sales data.  
Users can filter data by **Category**, **Sub-Category**, **Region**, and **Segment**, then run specific queries to view results such as total sales, average sales, or top products.

The app uses a CSV file (`TableauSalesData.csv`) as its backend database and dynamically generates dropdowns based on unique values in the dataset.

---

## Features
- **Interactive Filters** for:
  - Category
  - Sub-Category
  - Region
  - Segment  
- **Predefined Queries**:
  - Total Sales  
  - Average Sales  
  - Top 5 Products by Sales  

The app filters the dataset based on user selections and displays results clearly on the results page.

---

## Project Structure
```
my_flask_app/
├── app.py
├── TableauSalesData.csv
├── templates/
│   ├── index.html
│   └── results.html
└── README.md
```

---

## Setup Instructions

### 1. Install Required Packages
Make sure you have Python installed (version 3.8+ recommended).  
Then install dependencies:

```bash
pip install flask pandas pyngrok
```

---

### 2. Add the Data File
Place the provided `TableauSalesData.csv` file in the same directory as `app.py`.

---

### 3. Run the Application
Run the Flask app using:

```bash
python app.py
```

If running locally, open your browser and visit:
```
http://127.0.0.1:5000
```

If using **Google Colab**, the app will start with a **public URL** provided by **ngrok**. This will look like:
```
🌍 Public URL: https://xxxxxx.ngrok.io
```
# Add your ngrok authtoken here. Get it from https://dashboard.ngrok.com/get-started/your-authtoken
# For example: ngrok.set_auth_token("YOUR_AUTHTOKEN")

---

### 4. Using the App
1. Open the application in your web browser.  
2. Use the dropdown menus to select:
   - Category
   - Sub-Category
   - Region
   - Segment
   - Query type  
3. Click **Submit** to view the results on a new page.

---

## What the App Does

- Loads and processes the **Superstore sales dataset** using **Pandas**.
- Dynamically populates dropdowns for filtering options.
- Performs calculations and displays results based on selected query:
  - **Total Sales:** Sums the `Sales` column for the filtered subset.
  - **Average Sales:** Calculates the mean of the `Sales` column.
  - **Top 5 Products by Sales:** Groups by product and lists the top 5 based on total sales.

---

## Learning Objectives
By completing this project, you will:
- Gain hands-on experience with **Flask** and **Pandas**.
- Learn how to connect **front-end forms** with **back-end data analysis**.
- Practice structuring code and debugging Flask applications.
- Develop comfort using **AI tools** (like GPT) for problem-solving, code enhancement, and debugging.

---

## Notes
- The app runs in **debug mode** for easier troubleshooting.
- Ensure that column names in the dataset match those expected by the script (`Category`, `Sub-Category`, `Region`, `Segment`, `Sales`, and `Product Name`).
