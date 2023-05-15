# Mars_News_and_Weather
<h2><b>Challenge 11:</b></h2><ol><li>Data collection using web-scraping of mars news and of temperature records from the Mars Curiosity Rover data from Mars_Facts website</li>
<li>Analysis of Mars News and Weather Data</li></ol> 
<p><h2>Assignment consists of two parts.</h2></p>
<p><b>Method</b></p>
<p><h3>Part 1:  Scrape titles and preview text from Mars news articles.</h3></p><ol>
  <li>Use Jupyter Notebook to write code
  <li>Automated browsing to scrape Mars News website - https://static.bc-edx.com/data/web/mars_news/index.html</li>
  <li>Beautiful Soup object used to extract text elements from website - article headings and preview text.</li>
  <li>Results stored in Python dictionary as title-preview pairs with keys: 'title' and 'preview'. Dictionary pairs stored in list</li>
  <li>Results printed to notebook and exported to a JSON file.</li></ol></p>
<p><h3>Part 2: Scrape and analyse Mars weather data</h3><p><ol>
<p><b>Method</b><p>
  <li>Jupyter Notebook used to write code</li>
  <li>Automated browsing to scrape Mars Temperature Data website: https://static.bc-edx.com/data/web/mars_facts/temperature.html</li>
  <li>Data contained in table. Beautiful Soup object used to scrape data in HTML table</li>
  <li>Scraped data assembled into Pandas DataFrame with headings:</li><ul>
  <li><b>id</b> - the identification number of a single transmission from the Curiosity rover</li><li><b>terrestrial_date</b> - the date on Earth</li>
    <li><b>sol</b> - the number of elapsed sols (Martian days) since Curiosity landed on Mars</b></li><li><b>ls</b> - the solar longitude</li>
    <li><b>month</b> - the Martian month</li><li><b>min_temp</b> - the minimum temperature, in Celsius, of a single Martian day (sol)</li>
    <li><b>pressure</b> - The atmospheric pressure at Curiosity's location</li></ul>
  <li>In preparation for analysis datatypes were checked and changed from 'object' to 'datetime', 'int' or 'float' as appropriate.</li>
  <li>Data rows checked for nulls</li>
  <li>A number of questions were answered by analysing the dataset and answered within the notebook</li><ul>
    <li>How many months exist on Mars? - 12 months</li>
    <li>How many Martian (and not Earth) days worth of data exist in the scraped dataset? 1867 Martian days</li>
    <li>What are the coldest and the warmest months on Mars (at the location of Curiosity)? - Coldest month is month 3 (avg. temperature of -83.3'C), and 'warmest' month is month 8 (avg. temperature of -68.4'C).</li><ul>
      <li>Mean temperature calculated for each month and plotted on a bar graph from lowest to highest temperature.</li>
      <li>Result confirmed by querying the DataFrame using .idxmax and .idxmin.</li></ul>
    <li>Which months have the lowest and the highest atmospheric pressure on Mars?  - atmospheric pressure is lowest in month 6 and highest in month 9.</li><ul>
      <li>Applied same method used in calculating min. and max. temperatures</li></ul> 
    <li>Estimate how many terrestrial (Earth) days exist in a Martian year?</li><ul>
      <li>Calculated using the elapse of earth days over the period of time Mars took to orbit the sun once.</li>
      <li>The first value of solar longitude in the DataFrame was calculated along with the index value of the second occurrence. The terrestrial dates for each occurrence were calculated and a timedelta function employed to return the nubmer of days elapsed - approx. 686.</li>
      <li>To provide a visual estimate the daily minimum temperatures for the dataset were plotted, giving an estimate of 675 days in a martian year.</li></ul></ul></ol>
  
  <p><h3><b>Sources</b></h3><p>
    <ul><li>https://stackoverflow.com/questions/22132525/add-column-with-number-of-days-between-dates-in-dataframe-pandas</li>
    <li>https://stackoverflow.com/questions/37840812/pandas-subtracting-two-date-columns-and-the-result-being-an-integer</li>
    <li>https://stackoverflow.com/questions/65048547/how-to-get-number-of-days-between-two-dates-using-pandas</li>
    <li>https://bramtunggala.medium.com/a-simple-way-to-finding-the-difference-between-two-dates-in-pandas-179d2714b6c</li>
    li>https://realpython.com/beautiful-soup-web-scraper-python</li>
    <li>https://opensource.com/article/21/9/web-scraping-python-beautiful-soup</li>
    <li>https://medium.com/geekculture/web-scraping-tables-in-python-using-beautiful-soup-8bbc31c5803e</li>
    <li>https://docs.python.org/3/library/datetime.html</li>
    <li>https://www.simplilearn.com/tutorials/python-tutorial/index-in-python</li>
    <li>https://stackoverflow.com/questions/54255890/how-to-find-the-row-index-of-the-first-occurrence-of-a-match-in-a-cell-in-python</li>
    <li>https://stackoverflow.com/questions/54255890/how-to-find-the-row-index-of-the-first-occurrence-of-a-match-in-a-cell-in-python]       (https://realpython.com/iterate-through-dictionary-python/)</li></ul>
