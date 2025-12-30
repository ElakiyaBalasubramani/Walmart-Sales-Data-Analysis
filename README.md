# Walmart Sales Data Analysis

This project performs Exploratory Data Analysis (EDA) on Walmart sales data and exports the processed information to a MySQL database for further querying and reporting.

## Project Structure

```text
walmart-project/
├── Data/
│   └── Walmart.csv              # Raw sales dataset
├── notebook/
│   ├── EDA.ipynb               # Data cleaning and exploratory analysis
│   └── walmart_clean_data.csv   # Processed and cleaned dataset
├── walmart/
│   ├── requirements.txt        # Python dependencies
│   └── venv/                   # Virtual environment (optional)
└── mysql-init.sql              # MySQL initialization script
```

## Features

- **Data Cleaning**: Handling missing values, removing duplicates, and correcting data types.
- **Exploratory Data Analysis**: Analyzing sales trends across different branches, cities, and categories.
- **Database Integration**: Exporting cleaned data to a MySQL database using `SQLAlchemy` and `PyMySQL`.

## Setup Instructions

### 1. Prerequisites
- Python 3.x
- MySQL Server

### 2. Install Dependencies
Navigate to the project directory and install the required Python packages:
```bash
pip install -r walmart/requirements.txt
```

### 3. Database Setup
Ensure your MySQL server is running. You can use the provided `mysql-init.sql` to initialize your database user or run your own configuration. The notebook expects a database named `walmart_db`.

### 4. Running the Analysis
Open the Jupyter Notebook to view and run the analysis:
```bash
jupyter notebook notebook/EDA.ipynb
```

## Data Overview

The dataset contains the following key columns:
- `invoice_id`: Unique identifier for each transaction
- `Branch`: Walmart branch identifier
- `City`: Location of the branch
- `category`: Product category
- `unit_price`: Price per unit
- `quantity`: Number of units sold
- `date` & `time`: Transaction timestamp
- `payment_method`: Method of payment (Cash, Ewallet, Credit card)
- `rating`: Customer rating
- `profit_margin`: Profit percentage per transaction
- `total`: Calculated total sales (unit_price * quantity)

## Author
**Elakiya Balasubramani**
