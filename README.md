# Real Time Stock Price ETL Data Pipeline

This repository contains the implementation of a real-time stock price ETL (Extract, Transform, Load) pipeline using Yahoo Finance API, Python, MongoDB, and Apache Airflow. The pipeline processes stock data from major companies, performs transformations, and loads the data into a MongoDB Atlas database. Finally, the data is visualized using Power BI.

## Architecture Overview


The architecture includes the following steps:
1. **Extract:** Retrieve real time stock data using the Yahoo Finance API.
2. **Transform:** Process the data in Python to calculate moving averages and daily returns.
3. **Load:** Store the processed data into MongoDB Atlas.
4. **Visualize:** Use Power BI to create dashboards and insights from the data.

## Features
- Extracts stock data for 17 major companies (e.g., Apple, Nvidia, Microsoft).
- Calculates technical indicators, including 5-day and 30-day moving averages.
- Computes daily percentage returns for each stock. 
- Stores the processed data in MongoDB Atlas for persistence and visualization.

## Technologies Used
- **Python** for data extraction and transformation.
- **Yahoo Finance API** for fetching real-time stock data.
- **MongoDB Atlas** for storing and querying stock data.
- **Apache Airflow** for scheduling and automating the ETL pipeline.
- **Power BI** for data visualization.

## Project Setup

### Prerequisites
- Python 3.7+
- MongoDB Atlas account
- Power BI desktop (for visualization)
- Libraries: `yfinance`, `pandas`, `pymongo`, `datetime`

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Youssef-Lamadi/Real-Time-Stock-Price-Data-Pipeline.git
   cd Real-Time-Stock-Price-Data-Pipeline
   ```

2. Install dependencies:
   ```bash
   pip install yfinance pandas pymongo
   ```

3. Configure MongoDB Atlas:
   - Create a cluster on MongoDB Atlas.
   - Replace the connection string in the code with your MongoDB credentials.

4. Run the ETL pipeline:
   ```bash
   python getDataFromMarket_LoadToMngDBAtlas.py
   ```

5. Set up Power BI:
   - Connect Power BI to MongoDB Atlas.
   - Design your dashboard using the processed stock data.

## Code Explanation
The main steps in the code:
1. **Extract Data:**
   - Use the Yahoo Finance API to fetch stock prices for the last two years for a predefined list of companies.

2. **Transform Data:**
   - Add 5-day and 30-day moving averages.
   - Calculate daily returns and clean missing values.

3. **Load Data:**
   - Store the processed data in MongoDB Atlas, replacing old data.

## Future Enhancements
- Implement additional indicators like RSI and MACD.
- Automate pipeline scheduling using Apache Airflow.
- Integrate real-time notifications for significant stock price changes.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Contact
For questions or collaboration, feel free to contact:
- **Email:** yousseflamadi3@gmail.com
- **LinkedIn:** [LinkedIn Profile](https://www.linkedin.com/in/youssef-lamadi-0257b6261/)

