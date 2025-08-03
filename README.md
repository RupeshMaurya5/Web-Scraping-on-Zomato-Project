# 🍽️ Web Scraping on Zomato Project

This project focuses on extracting detailed restaurant data from Zomato — one of India's leading platforms for restaurant discovery and food delivery. The scraper navigates through a Zomato **city page** and collects valuable restaurant-level information, including menus, prices, and contact details.

> ✅ **Note:** This project was developed and executed using **Anaconda Jupyter Notebook** for an interactive and modular coding experience.

---

## 🚀 What Does This Project Do?

The scraper collects the following data from restaurants listed on a Zomato city page:

- ✅ Restaurant Name  
- ✅ Zomato Restaurant URL  
- ✅ Address  
- ✅ Phone Number  
- ✅ Menu Category  
- ✅ Dish Name  
- ✅ Price  
- ✅ Type (Veg / Non-Veg)

---

## ⚙️ How Does the Code Work?

The project is divided into two notebook files:

### 1️⃣ `zomato_scraper.ipynb`
This is the **main scraping file** and performs the following steps:

1. **Library Import**  
   - Uses `pandas`, `BeautifulSoup`, `Selenium`, and `requests`.  
   - All dependencies are listed in the `requirements.txt` file.

2. **City Page URL Input**  
   - You manually input a Zomato city URL that leads to a restaurant listing page.

3. **Headless Browser Initialization**  
   - Launches a headless Chrome browser using Selenium to simulate user activity.

4. **Dynamic Scrolling**  
   - Scrolls automatically until all restaurants are loaded (Zomato uses lazy loading).

5. **Restaurant Listing Extraction**  
   - Extracts restaurant names and URLs from the city page using `BeautifulSoup`.

6. **Detailed Restaurant Info Scraping**  
   - For each restaurant:
     - Address
     - Phone number(s)
     - Menu items, prices, type (Veg/Non-Veg), category

7. **Data Export**  
   - All collected data is stored in a `pandas` DataFrame and exported as `zomato_restaurant_data.csv`.

---

### 2️⃣ `image_scraper.ipynb` *(Optional)*

This notebook extracts **food item images** from a single restaurant menu page:

- Accepts one restaurant menu URL as input  
- Scrolls through the menu page  
- Downloads images with proper food item names  
- Stores them in the `menu_images/` directory

> 🔸 This notebook is **independent** and can be run separately if images are required.

---

## 📁 Output Structure

The main output CSV will include the following columns:

- `name`  
- `url`  
- `address`  
- `phone_numbers`  
- `category`  
- `dish_name`  
- `price`  
- `type` (Veg / Non-Veg)

---

## 🧪 Environment & Tools

| Component        | Version / Note         |
|------------------|------------------------|
| Python           | 3.x (tested on 3.10+)  |
| Jupyter Notebook | via Anaconda Navigator |
| Browser          | Google Chrome          |
| Driver           | ChromeDriver (path must be set) |
| Platform         | Windows 10 (tested)    |

---
