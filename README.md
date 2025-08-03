# 🍽️ Web Scraping on Zomato Project
This project focuses on extracting detailed restaurant data from Zomato, one of India's leading platforms for restaurant discovery and food delivery. The scraper navigates through a Zomato city page and collects valuable restaurant-level information, including menus, prices, and contact details.

✅ Note: This project was developed and executed using Anaconda Jupyter Notebook for an interactive and modular coding experience.

🚀 What Does This Project Do?
The scraper collects the following data from restaurants listed on a Zomato city page:
✅ Restaurant Name
✅ Zomato Restaurant URL
✅ Address
✅ Phone Number
✅ Menu Category
✅ Dish Name
✅ Price
✅ Type (Veg / Non-Veg)

⚙️ How Does the Code Work?
1. Library Import
- Required libraries such as pandas, BeautifulSoup, Selenium, and requests are imported. All dependencies are listed in the requirements.txt file.

2. City Page URL Input
- The Zomato city URL is manually provided in the notebook. This URL points to the restaurant listing page for a specific city or locality.

3. Headless Browser Initialization
- A headless Chrome browser is launched using Selenium to simulate human behavior and avoid bot detection.

4. Dynamic Scrolling
- Zomato loads restaurant data lazily as the user scrolls. The scraper mimics this behavior by scrolling programmatically until all content is loaded.

5. Restaurant Listing Extraction
- Once the page content is fully loaded, BeautifulSoup is used to parse and extract:
- Restaurant names
- Restaurant profile URLs

6. Detailed Information Extraction
- For each restaurant, the following is scraped:
- Address
- Phone number(s)
- Menu items
- Prices
- Category and type (Veg / Non-Veg)

7. Data Aggregation and Export
- The extracted data is stored in pandas DataFrames and exported to a CSV file (zomato_restaurant_data.csv).

📁 Output Format
The resulting dataset includes columns such as:
- name
- url
- Address
- Phone Numbers
- Category
- Dish Name
- Price
- Type

🧪 Environment
This project was created and run in:
- Anaconda (Python 3.x)
- Jupyter Notebook
- Compatible with Windows (tested with ChromeDriver)
