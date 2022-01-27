# Scrapping Data
This data is a review of one of the applications on the Google Play Store, namely Quipper.
One of the files contains reviews that have been labeled as positive or negative sentiment categories.
These reviews were taken using google-play-scrapper.
The reviews taken are only in Indonesian Language.

```python
pip install google-play-scraper

from google_play_scraper import reviews_all
Quipper = reviews_all(
    'com.quipper.school.assignment,
    sleep_milliseconds=0,
    lang='id', # defaults to 'en'
    country='id', # defaults to 'us'
    sort=Sort.NEWEST, # defaults to Sort.MOST_RELEVANT
    count=200)
 
import pandas as pd 
df = pd.DataFrame(Quipper)
df.to_csv('/content/Quipper.csv')
```
