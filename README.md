# ecom-data-finder
A Streamlit-powered tool for discovering e-commerce business websites and extracting contact emails.

Overview

    E-Com Data Finder assists the user in discovering e-commerce websites by industry, state/city, and country through Google Search through SerpAPI.
    It further facilitates filtering websites (active, Shopify-based, fast-loading) and pulling contact email addresses automatically.

The tool proves to be especially helpful for:

    Lead generation

    Market research

    Business development

    Competitor analysis

Key Features

    ✅ Google Search Integration – Returns relevant websites using SerpAPI.
    ✅ Smart Filtering – Filter websites that are:
    Active (domain reachable)
    Built on Shopify
    Load within 5 seconds
        ✅ Email Extraction – Automatically extracts email addresses from websites fetched.
        ✅ CSV Export – Download all websites, filtered lists, or extracted emails as CSV files.
        ✅ Interactive UI – Implemented with Streamlit using a clean and intuitive design.

Tech Stack
    Component	Technology
    Frontend UI	Streamlit
    Backend	Python
    Data Extraction	Requests, BeautifulSoup, Regex
    Search API	SerpAPI
    Data Handling	Pandas
    Deployment	Streamlit Cloud (recommended)

⚙️ Installation & Setup
    1️⃣ Clone the Repository
        git clone https://github.com/your-username/ecom-data-finder.git
        cd ecom-data-finder

    2️⃣ Install Dependencies

        Make sure you have Python 3.9+ installed.
        pip install -r requirements.txt
        Example requirements.txt:

            streamlit
            pandas
            requests
            beautifulsoup4
            serpapi

    3️⃣ Set Your SerpAPI Key

        Swap your key within the code or store it as an environment variable:
        export SERPAPI_KEY="your_api_key_here"

    4️⃣ Run the App
        streamlit run app.py

Project Structure
    E-Com-Data-Finder/
    │
    ├── app.py                     # Main Streamlit application
    ├── requirements.txt           # Dependencies
    ├── README.md                  # Documentation
    ├── frontend                   #frontend code  

Usage Guide
    Step 1: Fetch Websites

        Input:

          Country (e.g., India, USA)

          State or City (e.g., Texas, Maharashtra)

          Industry (e.g., Eyeglasses Store, Coffee Shop)

          Number of results to fetch (max 1000)

          Click -----> Fetch Websites to retrieve URLs and save as websites_raw.csv.

    Step 2: Filter Websites

        Use filters:
            Active websites
            Shopify stores
            Load within 5 seconds
            Then click -----> Exclude Sites & Filter → download filtered_websites.csv.

    Step 3: Extract Emails

Upload your filtered CSV file → click -----> Fetch Email IDs → get all found emails → download emails.csv.

Output Files
    File Name	Description
    websites_raw.csv	All fetched website URLs
    filtered_websites.csv	After applying filters
    emails.csv	Extracted website-email pairs

API Usage Note
    This project uses the SerpAPI free/paid key for fetching Google search results.
    Visit SerpAPI
    to get your API key.
    Make sure to follow SerpAPI's terms and usage limits.

Future Scope / Possible Improvements

   Include domain categorization or tech stack detection

   Bing / DuckDuckGo API as fallback support

   Incorporate data visualization dashboards

   Incorporate AI-powered email verification

☁️ Store results in SQLite or Firebase to track history

   Author:
    Rashmi G.
    Developed as part of a coding challenge.
