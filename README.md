```markdown
# SEC 10-K Data Scraper

This project provides a Python script to extract and process data from the SEC's EDGAR system. The script uses company CIK numbers to fetch 10-K filing data and parses specific information for further analysis.

## Features
- Fetches 10-K filings for a given list of CIK numbers.
- Extracts and displays filing type, filing date, and document links.
- Processes HTML content from the filing links.
- Updates an Excel sheet with extracted data.

## Prerequisites
Before running the script, ensure you have the following:
- Python 3.x installed.
- The following Python libraries:
  - `requests`
  - `pandas`
  - `bs4` (BeautifulSoup)

You can install the required libraries using pip:
```bash
pip install requests pandas beautifulsoup4
```

## Getting Started
1. **Clone the Repository**  
   Clone this repository to your local machine:
   ```bash
   git clone https://github.com/SanaullahKayani/Web-Scrapping
   cd repo-name
   ```

2. **Prepare Your Data**  
   Create an Excel file (`short_file.xlsx`) containing a column `CIK` with company CIK numbers.

3. **Update the File Path**  
   Update the `df = pd.read_excel()` line with the correct path to your Excel file.

4. **Run the Script**  
   Execute the script:
   ```bash
   python your_script_name.py
   ```

5. **Results**  
   The script will scrape the SEC EDGAR system for each CIK number in the Excel file, extract filing data, and update the Excel file with additional details.

## Key Functions
- `ertract_data(CIK_no)`  
   This function takes a CIK number, scrapes the SEC EDGAR website for 10-K filings, extracts document links, and updates the corresponding row in the Excel file with extracted data.

## Notes
- The script currently processes only 10-K filings.
- Ensure the SEC's website is accessible and there are no network restrictions.
- The SEC website enforces rate limits; excessive requests may result in temporary blocking.

## File Structure
```
repo-name/
│
├── short_file.xlsx    # Input Excel file with CIK numbers
├── script.py          # Main Python script
└── README.md          # Project documentation
```

## Example Output
The script prints filing details in the terminal:
```
----------------------------------------------------------------------------------------------------
Filing Type: 10-K
Filing Date: 2023-01-15
Filing Number: 1234567890
Document Link: https://www.sec.gov/...
Filing Number Link: https://www.sec.gov/...
Interactive Data Link: https://www.sec.gov/...
```

The updated Excel file includes the extracted data for each CIK.

## License
This project is licensed under the MIT License.

## Contributing
Contributions are welcome! Feel free to fork the repository and submit a pull request.

## Contact
For any questions or issues, please reach out to [Your Email/Contact Info].

---

Happy Scraping!
```

Make sure to replace placeholders like `your-username`, `repo-name`, `your_script_name.py`, and `[Your Email/Contact Info]` with your actual details.
