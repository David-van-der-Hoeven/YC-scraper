# YC-scraper
Script to scrape the YoungCapital job vacancies website, using geocoding to attach a region and visualize it on a map of the Netherlands

I was curious to know which regions in the Netherlands have the most job oppertunities and where people are paid the most. To that end I created this script to determine the provinces with the best employment oppertunities.

First I send an HTTP request to the main search page and extract the page source, which gets fed into beautifulsoup and used to determine the number of search results. This determines the maximum number of pages that can be scraped. The user is then asked to input the number of pages to be looked up.

The script then looks up that number of pages, extracts the vacancies with their location, salary and emplopyment form and forms it into a dataframe. Positionstack is used to attach province information to the locations. A map of the Netherlands with geographical boundaries is imported as a geopandas dataframe. This gpd df is merged with the vacancies dataframe, and finally it is plotted onto the map of the Netherlands.

From this it is easy to see that most of the job oppertunities are in the west of the Netherlands, with Noord-Holland easily coming in first place. The highest paid job openings also tend to be in the Noord-Holland area.
