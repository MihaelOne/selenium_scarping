### Project Title: Amazon Product Scraper

---

#### Project Overview

This project contains a Jupyter Notebook script that scrapes product information from Amazon using Selenium. The script is designed to scrape data across multiple pages (in this case, 24 pages) of search results. It saves the scraped data into both CSV and Excel formats.

### Files Included

1. **`selenium_web_scraping.ipynb`**: 
   - This is the main Jupyter Notebook containing the Selenium-based web scraping script. The script scrapes product information from Amazon search results and saves the data in CSV and Excel formats.

2. **`amazon_products.csv`**:
   - This file contains the scraped product data in CSV format. Each row represents a product, and each column represents different attributes of the product (e.g., name, price, rating, etc.).

3. **`amazon_products.xlsx`**:
   - This file contains the scraped product data in Excel format, similar to the CSV file but stored in an Excel spreadsheet. Each sheet contains data organized by columns corresponding to product attributes.

### Usage Instructions

#### Setup

1. **Environment Setup**:
   - Install the necessary Python packages by running the following command:
     ```bash
     pip install selenium pandas openpyxl
     ```
   - Download and install the appropriate WebDriver for your browser (e.g., ChromeDriver for Google Chrome). Ensure that the WebDriver is added to your system's PATH.

2. **Running the Script**:
   - Open the `selenium_web_scraping.ipynb` file in Jupyter Notebook.
   - Run the cells sequentially to execute the script.
   - The script will navigate to Amazon, search for a specific product (e.g., laptops), and scrape product data across multiple pages.

3. **Output**:
   - The scraped data will be saved in two files:
     - `amazon_products.csv`: A CSV file containing the scraped data.
     - `amazon_products.xlsx`: An Excel file containing the scraped data.

#### Customization for a Different Category

To scrape products from a different category or search term, follow these steps:

1. **Modify the Search Term**:
   - In the Jupyter Notebook, locate the section where the search term is defined:
     ```python
     search_box.send_keys("laptop")
     ```
   - Replace `"laptop"` with your desired search term. For example, if you want to scrape data for "smartphones", change it to:
     ```python
     search_box.send_keys("smartphone")
     ```

2. **Adjust the Number of Pages**:
   - By default, the script is set to scrape 24 pages. If you want to scrape more or fewer pages, locate the loop controlling page navigation:
     ```python
     for page in range(1, 25):  # Currently set to scrape 24 pages
     ```
   - Adjust the number to your preference. For example, to scrape 10 pages:
     ```python
     for page in range(1, 11):
     ```

3. **Run the Script**:
   - After making the necessary adjustments, re-run the cells in the Jupyter Notebook to scrape data for the new search term or category.

### Considerations

- **Captcha Handling**: Amazon may present captchas if it detects automated scraping. If this occurs, you may need to manually solve the captcha before the script can continue.
- **Ethical Scraping**: Ensure you comply with Amazon's terms of service when scraping data.

### Conclusion

This project provides a powerful and flexible solution for scraping Amazon product data. By following the instructions above, you can adapt the script to scrape data for different products or categories, saving the output in both CSV and Excel formats for further analysis.

---

This README guide provides a comprehensive overview of the project, its files, and how to customize and execute the scraping script.
