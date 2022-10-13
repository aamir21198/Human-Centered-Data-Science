# Considering Bias in Data

**DATA 512: Human-Centered Data Science**

**Homework 2**

[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/aamir21198/Human-Centered-Data-Science/blob/main/LICENSE)

The goal of this assignment is to explore the concept of bias in data using Wikipedia articles. This assignment will consider articles on political figures from different countries.

Data Scraped from:
- [Category:Politicians by nationality](https://en.wikipedia.org/w/index.php?title=Category:Politicians_by_nationality&subcatfrom=South+Sudanese+politicians#mw-subcategories).
- [World Population Data Sheet](https://www.prb.org/international/indicator/population/table)

WikiMedia API:
- Documentation: [API:Info](https://www.mediawiki.org/wiki/API:Info)
- License: [Creative Commons Attribution-ShareAlike License](https://creativecommons.org/licenses/by-sa/3.0/)

ORES API:
- Documentation: [ORES](https://www.mediawiki.org/wiki/ORES)
- License: [Creative Commons Attribution-ShareAlike License](https://creativecommons.org/licenses/by-sa/3.0/)

### Input Data Files
- Data/politicians_by_country_SEPT.2022.csv.xlsx
  - List of politicians and their associated country.
- Data/population_by_country_2022.csv.xlsx
  - List of countries and their population in millions.

### Output Files
- Output/wp_countries-no_match.txt
  - List for countries in the politician and population data that do not find a match in the other data set.
- Output/wp_politicians_by_country.csv
  - Consolidated data of politician articles, their countries and region, the respective country population and article quality.

### Data Description for wp_politicians_by_country.csv

| Feature         | Data type | Description                                                                    |
|-----------------|-----------|--------------------------------------------------------------------------------|
| country         | String    | The country that the politician belongs to                                     |
| region          | String    | The region that the country belongs to                                         |
| population      | float     | Population of the respective country (in millions, rounded to 1 decimal place) |
| article_title   | String    | The Wikipedia article title of the politician (the politician's name)          |
| revision_id     | float     | The last revision ID of the Wikipedia article                                  |
| article_quality | String    | The quality of the article as predicted by the ORES API                        |

### Research Implications

I did not find the above analysis to be completely useful. The given list of articles scraped from Wikipedia does not contain politician articles from many countries, including major countries like the United States, Canada, Australia, United Kingdom, etc. No articles from the North America region are present. Most countries only have a few number of articles present, ignoring most of eminent political figures. Hence, I believe that the number of articles present is a bad indicator to use in order to make any insights.

However, despite these missing articles we can still make insights from the countries whose data is present, by comparing the total number of articles with the number of high quality articles. This gives us an idea that some countries have a higher ratio of high quality articles. These represent countries / regions having a bias towards high quality articles.

Countries having high populations, like India and China, have substantially lower number of articles per capita. European countries have comparatively lower populations and high number of politician articles. This must be because of their long-standing well-documented history. Hence, it is not surprising that all the European Regions happen to be at the top of the regions with most number of articles and high quality articles. I was surprised to see many caribbean countries having a large number of articles as well as high quality articles per capita.

We find that few regions climbed the ranking while considering only high quality articles, such as Eastern Europe and South-East Asia. On the other hand Oceania falls down when considering high quality articles. In the last chart of my analysis I calculate the ration of high quality articles for each region. Surprisingly, East Asia and South-East Asia happen to be have a higher ratio of high quality articles as compared to European regions. African and South American regions happen to be lower on this list. Hence, we do a see a high bias in rating East Asia, South-East Asian and European articles as compared to other regions.

1. What biases did you expect to find in the data (before you started working with it), and why?
- Initially, I expected to find a high bias of articles from the United States, Canada and United Kingdom to have a large ratio of high quality articles. However, I was surprised to find that the list of politician articles scrapped from Wikipedia does not contain articles from these countries. After knowing this I was expecting high biases towards the European regions due to their long-standing and well-documented history and comparatively lower populations. The results do confirm these biases.

2. What (potential) sources of bias did you discover in the course of your data processing and analysis?
- As mentioned above, I discovered a high bias against highly populated countries and regions. On the other hand, European countries having a large number of famous politicians and comparatively lower populations have more high quality articles indicating a bias.

3. What might your results suggest about (English) Wikipedia as a data source?
- Since Wikipedia is an English language encyclopedia, I was expected high biases towards English-speaking countries like the United States, Canada, United Kingdom, etc. However, the scrapped data omitted almost all English-speaking countries. That's why we notice high number of articles from the Caribbean islands, since they are primarily English-speaking countries.
- However, we can still continue to conclude that the presence of Wikipedia articles is biased towards the western world with European Regions having a large number of articles as well as high quality articles. These nations have a substantially higher contribution to Wikipedia.
