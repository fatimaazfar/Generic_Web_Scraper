# Generic Scraper Documentation

## Overview

This is a generic web scraper script written in Python, utilizing the `requests` library for HTTP requests and `BeautifulSoup` for HTML parsing. The scraped data is organized into a Pandas DataFrame and exported to a CSV file. This scraper was built for this website: https://www.webstaurantstore.com

## Usage

1. Install the required libraries:

    ```bash
    pip install requests
    pip install beautifulsoup4
    pip install pandas
    ```

2. Update the script with the URLs you want to scrape:

    ```python
    urls = unique_links
    ```

3. Run the script:

    ```bash
    python your_scraper_script.py
    ```

## Dependencies

- `requests`: Used for making HTTP requests.
- `BeautifulSoup`: Used for parsing HTML content.
- `pandas`: Used for organizing and manipulating data.

## Script Details

### Data Columns

The script extracts the following data columns:

- **Link**: The URL of the scraped page.
- **Taxonomy**: Breadcrumb navigation of the page.
- **H1 Title**: The main heading of the page.

Additional columns are dynamically generated based on the filters found on the page.

### Error Handling

The script handles both request and processing errors. URLs that encounter errors are logged in the `error_urls.txt` file.

### Output

The scraped data is saved in a CSV file named `data3.csv`.

## Customization

Feel free to customize the script according to your specific needs. You can modify the script to add or remove data columns based on the structure of the websites you are scraping.

```python
# Customization Example:
# Add a new data column
data_columns.append("New Column")
# Update the DataFrame
filter_dict["New Column"] = "Some Value"
```
Remember to review and adhere to the terms of service of the websites you are scraping.

Happy scraping!
