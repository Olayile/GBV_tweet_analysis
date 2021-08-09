# GBV_tweet_analysis

Can you classify tweets about GBV without using keywords?
---

## Trigger warning: The data in this competition can contain graphic descriptions of or extensive discussion of abuse, especially sexual abuse or torture.

Submitted to :  Gender-Based Violence Tweet Classification by #ZindiWeekendz



## Exploratory data analysis done on the tweets column

### STEP 1: Cleaning data
```py
def clean_text(text):
    '''Make text lowercase, remove text in square brackets,remove links,remove punctuation
    and remove words containing numbers.'''
    text = text.lower()
    text = re.sub('\[.*?\]', '', text)
    text = re.sub('https?://\S+|www\.\S+', '', text)
    text = re.sub('<.*?>+', '', text)
    text = re.sub('[%s]' % re.escape(string.punctuation), '', text)
    text = re.sub('\n', '', text)
    text = re.sub('\w*\d\w*', '', text)
    return text
    
 ```

