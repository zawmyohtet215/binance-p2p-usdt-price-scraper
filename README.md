# binance-p2p-usdt-price-scraper
Binance P2P USDT Price Scraper
### Project Description: Binance P2P USDT Price Scraper

#### Project Overview
This project involves developing a Python script that automates the extraction of USDT (Tether) prices in USD from Binance's P2P (peer-to-peer) trading platform. The script uses Selenium to interact with the web interface, scrape relevant data, and store it in a PostgreSQL database for further analysis and monitoring.

#### Key Features
1. **Web Scraping with Selenium**:
   - Initiates a Selenium WebDriver instance to navigate Binance's P2P trading page.
   - Accepts cookies to comply with website requirements.
   - Selects a refresh interval to ensure timely updates.

2. **Data Extraction**:
   - Extracts details from the "buy" and "sell" advertisements listed on the platform, including the name of the trader, price per USDT, trade volume in USDT, and the minimum and maximum transaction limits.
   - Captures the best price and volume as well as calculates the average price and total volume of the top four listings.

3. **Data Storage**:
   - Transforms the scraped data into a Pandas DataFrame.
   - Inserts the DataFrame into a PostgreSQL database, ensuring that data is stored efficiently and can be retrieved for analysis.

4. **Error Handling and Logging**:
   - Implements robust error handling to manage and log exceptions during execution.
   - Uses Python's logging module to log the script's activity, which helps in monitoring the script's performance and troubleshooting issues.

5. **Automated Execution**:
   - Runs in a continuous loop with a set interval, regularly updating the data stored in the database to reflect the latest prices on Binance's P2P platform.

#### Technical Details
- **Programming Language**: Python
- **Libraries and Tools**:
  - `selenium`: For web scraping and interacting with the Binance P2P platform.
  - `pandas`: For data manipulation and DataFrame creation.
  - `sqlalchemy`: For database connection and data insertion.
  - `logging`: For logging script activities and errors.
- **Database**: PostgreSQL

#### Setup and Usage
1. **Prerequisites**:
   - Python 3.x
   - WebDriver for Selenium (e.g., GeckoDriver for Firefox)
   - PostgreSQL database with appropriate user credentials and permissions.

2. **Installation**:
   - Install required Python packages using pip:
     ```bash
     pip install selenium pandas sqlalchemy psycopg2
     ```

3. **Configuration**:
   - Update the `db_config` dictionary in the script with your PostgreSQL database connection details.

4. **Execution**:
   - Run the script:
     ```bash
     python binance_p2p_scraper.py
     ```

5. **Monitoring**:
   - Monitor the script's logs to ensure it is running correctly and data is being updated in the database.

#### Potential Use Cases
- **Market Analysis**: Provides real-time data for market analysts to study trends in P2P trading of USDT on Binance.
- **Arbitrage Opportunities**: Identifies potential arbitrage opportunities by comparing buy and sell prices.
- **Price Monitoring**: Helps traders and investors keep track of the latest prices and make informed trading decisions.

#### Future Enhancements
- **Notification System**: Integrate a notification system to alert users when significant price changes occur.
- **Advanced Analytics**: Implement additional data analytics features to provide deeper insights into trading patterns.
- **User Interface**: Develop a user-friendly interface to visualize the data and trends in real-time.
