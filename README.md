<H3>NAME : SANJAY T</H3>
<H3>REGISTER NUMBER : 212222110039</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective :</H3>
  
Perform sentiment analysis using your Facebook data and filter the data that has only Positive feedback for the code given in the following link.

<H3>Program:</H3>
  
```py
pip install pandas textblob nltk

import pandas as pd
from textblob import TextBlob

# Sample DataFrame simulating Facebook data
data = {
    'post_id': [1, 2, 3, 4],
    'content': [
        'I love the new update!',
        'This is the worst experience ever.',
        'The app is okay, not great.',
        'Absolutely terrible support!'
    ]
}

# Create DataFrame
df = pd.DataFrame(data)

# Function to classify sentiment
def get_sentiment(text):
    analysis = TextBlob(text)
    # Classifying sentiment: < 0 indicates negative sentiment
    if analysis.sentiment.polarity < 0:
        return 'negative'
    else:
        return 'positive'

# Apply the sentiment analysis function to the content
df['sentiment'] = df['content'].apply(get_sentiment)

# Filter for negative feedback
negative_feedback = df[df['sentiment'] == 'negative']

# Display negative feedback
print("Negative Feedback:")
print(negative_feedback[['post_id', 'content']])

```

<H3>Output:</H3>

![Screenshot 2024-11-01 203003](https://github.com/user-attachments/assets/5eded364-f31b-4d3f-85b4-9a23b51d4678)

<H3>Inference:</H3>
Thus sentiment analysis using Facebook data is done and filtering the data that has only positive feedback for the code is executed successfully.
