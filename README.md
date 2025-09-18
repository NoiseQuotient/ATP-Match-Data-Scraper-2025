# ATP Match Data Scraper 2025
This project scrapes detailed tennis match data for the 2025 ATP Tour, including scores, stats, head-to-head records, and metadata (tournament, round, surface, etc.) from the official [ATP Tour website](https://www.atptour.com). It uses **Selenium** and **BeautifulSoup** to extract structured data and saves it to an Excel file for further analysis or modeling. It basically automates the tedious job of clicking through tournament pages and match stats, so you get a clean, ready-to-use Excel file with all the info.

---

## How does it work?

Here’s a quick rundown of what the code does:

1. **Loads tournament pages**  
   It visits the results pages for a bunch of 2025 ATP tournaments (like Wimbledon, Miami, Roland Garros, and many more).

2. **Handles cookie pop-ups**  
   If the site asks you to accept cookies, the scraper clicks “Accept” automatically so it can keep going.

3. **Extracts tournament info**  
   It grabs the tournament name, surface type (grass, clay, hard court), and the start/end dates.

4. **Finds match rounds and dates**  
   The scraper looks at each round (like “Quarterfinal” or “Round of 16”) and figures out the date matches were played on.

5. **Gathers match details**  
   For every match, it collects:
   - Player names and country codes  
   - Match scores (including tiebreaks)  
   - Match duration  
   - Links to detailed stats pages

6. **Scrapes detailed stats**  
   For matches with stats pages, it pulls serve percentages, aces, double faults, break points, and more for both players.

7. **Fetches head-to-head data**  
   It also grabs historical head-to-head stats between the two players, like who’s won more matches and key shared stats.

8. **Cleans and normalizes data**  
   The code standardizes round names, computes match dates if missing, and figures out who won based on scores.

9. **Saves everything to Excel**  
   All the collected data is saved into a single Excel file (`ATP_2025_Competitions.xlsx`), appending new data if the file already exists.

---

## Why is this useful?

- **For tennis fans and analysts:** Get detailed, up-to-date match data without manual scraping.  
- **For data scientists:** Build machine learning models or statistical analyses with rich, clean data.  
- **For developers:** A solid example of using Selenium and BeautifulSoup together to scrape complex, dynamic websites.

---

## What do you need to run it?

- Python 3.8 or newer  
- Google Chrome installed  
- Python packages: `selenium`, `undetected-chromedriver`, `pandas`, `beautifulsoup4`, `openpyxl`

You can install the packages with:

```bash
pip install selenium undetected-chromedriver pandas beautifulsoup4 openpyxl
