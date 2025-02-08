StockWatch_CalcPro/
│
├── stockwatch/
│   ├── main.py                  # Main script for stock dashboard
│   ├── data_fetcher.py          # Script to fetch stock data
│   ├── visualizer.py            # Script for graphical representation
│   ├── alerts.py                # Script for market trend alerts
│   ├── database.py              # Script for database operations
│   ├── reports.py               # Script for generating reports
│   └── README.md                # Documentation for StockWatch
│
├── calcpro/
│   ├── main.py                  # Main script for calculator
│   ├── gui_calculator.py        # Optional GUI-based calculator
│   ├── history_logger.py        # Script for saving history
│   ├── reports.py               # Script for generating reports
│   └── README.md                # Documentation for CalcPro
│
├── requirements.txt             # List of dependencies
└── README.md                    # Overall project documentation



pip install matplotlib pandas requests sqlite3 tkinter
import requests

def fetch_stock_data(symbol, api_key):
  
    response = requests.get(url)
    data = response.json()
    return data
    import matplotlib.pyplot as plt

def plot_stock_prices(prices):
    plt.plot(prices)
    plt.title("Stock Price Trend")
    plt.xlabel("Time")
    plt.ylabel("Price")
    plt.show()
    def check_alert(price, threshold):
    if price > threshold:
        print(f"Alert: Price crossed {threshold}!")
        import sqlite3

def save_to_database(symbol, price, timestamp):
    conn = sqlite3.connect("stocks.db")
    cursor = conn.cursor()
    cursor.execute("CREATE TABLE IF NOT EXISTS stocks (symbol TEXT, price REAL, timestamp TEXT)")
    cursor.execute("INSERT INTO stocks VALUES (?, ?, ?)", (symbol, price, timestamp))
    conn.commit()
    conn.close()
    def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        raise ValueError("Cannot divide by zero!")
    return x / y
    try:
    result = divide(10, 0)
except ValueError as e:
    print(e)
    def save_history(operation, result):
    with open("history.txt", "a") as file:
        file.write(f"{operation} = {result}\n")
