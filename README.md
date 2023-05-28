# Mission to Mars

## Purpose
We will help Robin scrape, organize, and visualize the Mars data consisting of two technical products.
- Deliverable 1: Scrape titles and preview text from Mars news articles.
- Deliverable 2: Scrape and analyze Mars weather data, which exists in a table.
## Results

[Mars Website](https://redplanetscience.com/)

[Mars Temp Data](https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html)

### Part 1: Scrape Titles and Preview Text from Mars News

- Automated browsing (with Splinter) was used to visit the Mars news site, and the HTML code was extracted (with Beautiful Soup)

      obj_soup = soup(html, 'html.parser')
      obj_soup.head

- The titles and preview text of the news articles were scraped and extracted

      all_elements = obj_soup.find_all('div', class_ = 'list_text')
      all_elements

- The scraped information was stored in the specified Python data structure—specifically, a list of dictionaries

      mars_list = []
      for obj_soup in all_elements:
          title = obj_soup.find('div', class_='content_title').text
          preview = obj_soup.find('div', class_='article_teaser_body').text
          mars_list.append({'title': title, 'preview': preview})
    
## Part 2: Scrape and Analyze Mars Weather Data

The data was analyzed to answer the following questions: [Part 2](https://github.com/Jall3n/Mission2Mars_Mod11/blob/main/part_2_mars_weather.ipynb)

1. How many months exist on Mars? There are 12 months that exist on Mars.

2. How many Martian days' worth of data are there? There are 1,867 days worth of data available.

The data was analyzed to answer the following questions, and a data visualization was created to support each answer:

Which month, on average, has the lowest temperature? The highest?
Which month, on average, has the lowest atmospheric pressure? The highest?
How many terrestrial days exist in a Martian year? A visual estimate within 25% was made.

## Summary

## Resources
1. https://learnpython.com/blog/python-datetime-for-beginners/#:~:text=datetime%20%E2%80%93%20combines%20date%20and%20time,between%20two%20dates%20or%20times
2. https://courses.bootcampspot.com/courses/2957/pages/11-dot-6-2-scraping-mars-facts?module_item_id=870273
3. https://www.python-graph-gallery.com/2-horizontal-barplot

- ![#f03c15](https://placehold.co/15x15/f03c15/f03c15.png) `#f03c15`
- ![#c5f015](https://placehold.co/15x15/c5f015/c5f015.png) `#c5f015`
- ![#1589F0](https://placehold.co/15x15/1589F0/1589F0.png) `#1589F0`
