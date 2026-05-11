# BinThereNYC_Data

## Description
Data collection and interactive map visualization for recycling drop-off points in NYC. View the github site at https://kirstseg.github.io/BinThereNYC_Data/

## Rationale
New York City produces 13,000 tonnes of landfill waste each day - 75% of these item are recyclable. The goal of this project was to create a centralized drop-off locator for common recyclable items that are not accepted in DSNY curb-side pick-up. This project gathered drop-off point information (Sitename, Address, Borough, Latitude, Longitude, Category) for the select Waste Categories (Electronics, Batteries, Paint, Textiles, Pharmaceuticals, and Special Waste) 

## Data Collection Workflow

Libraries (and their use):
- Requests (Interacting with web servers)
- Pandas (Dataframes)
- Folium (Map Visualizations)
- Beautiful Soup > BS4 (Web Scraping)
- Geopy > Nominatim (Geocoding)
  
Techniques:

- Electronics, Special Waste, and Pharmaceuticals & Syringes:
  - API from NYC Open Data 

- Textiles:
  - Web Scraped from Grow NYC
  - Geo-Coded to obtain Latitude and Longitude information
  - Manually cleaned data to provide missing fields

- Batteries & Paint:
  - Network Scraping from the Battery Network and Paint Care
  - Cleaned list to only show desired fields and values in NYC Zip Codes

- For everything:
  - Created dataframe
  - Exported to CSV
  - Visualized in interactive map

## Files 
  - Textiles.ipynb (Web Scraping Textile Data, Outputting CSVs, Map Visualization)  
  - textiles.csv
  - textiles_updated.csv (*this was my SMALLEST dataset but took the most work and a lot of manual cleaning)
  - Batteries.ipynb (Network Scraping Battery Data, Outputting CSV, Map Visualization)  
  - batteries.csv  
  - Paint.ipynb (Network Scraping Paint Data, Outputting CSV, Map Visualization)  
  - paint.csv  
  - Electronics.ipynb (API Call for Electronics Data, Special Waste Data, and Pharmaceutical Data,Outputting CSVs for each, Map Visualization for each)  
  - electronics.csv  
  - special_waste.csv  
  - pharmaceuticals-syringes.csv  
  - NYC-ZIP.csv (for filtering out scraped data for only NYC locations) 

## Further uses
I combined all the CSVs into a single dataset and converted it into a json file and used leaflet.js to display the data as a single interactive map in a web application that allows users to locate a drop-off center near them based on boroughs and categories. It would be great for this project to grow to include more item types (eg. lightbulbs, furniture etc) to provide a more comprehensive service. 

Here are the files for the interactive Web App:

  - index.html (page structure)
  - styles.css (page styling)
  - Locations.json (data for interactive map)
  - Hero.png
  - Logo.png
