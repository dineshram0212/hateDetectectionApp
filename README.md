# Hate Speech Detection App

This Streamlit-based application retrieves tweets from a specified Twitter user profile and detects the presence of hate speech using a pre-trained machine learning model. It provides both profile-based tweet analysis and individual text input detection.

## Features

- **Profile Analysis**: Enter a Twitter user’s profile URL, retrieve tweets up to a specified time period, and flag instances of hate speech.
- **Individual Text Analysis**: Input custom text for quick hate speech detection.
- **Downloadable Results**: Download the predictions as a CSV file for further analysis.

## Machine Learning Model

The hate speech detection model used in this app is a supervised machine learning model trained on a labeled dataset of text data. This model applies natural language processing (NLP) techniques to identify patterns associated with hate speech. It uses tokenization and text preprocessing, and features have been extracted to train a binary classifier that outputs labels indicating the presence or absence of hate speech. The model (`model_final.pkl`) is saved and loaded using `pickle` for deployment in this app.

## Requirements

- Python 3.x
- Streamlit
- snscrape
- pandas
- scikit-learn
- unidecode

## Installation

1. **Clone the Repository**
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

3. **Download or place the pre-trained model** `model_final.pkl` in the root directory of the repository.


## Code Overview

- **getTweets**: Extracts tweets from a Twitter user profile based on the provided URL and limit.
- **predictdf**: Cleans tweet text data and applies the hate speech model to detect hate speech in each tweet.
- **predictText**: Detects hate speech in a single text input.
- **convert_df**: Converts the DataFrame to CSV format for download.

## License

This project is licensed under the MIT License.

---

This application combines NLP and machine learning for efficient hate speech detection, offering quick insights into the presence of hate speech in social media text.
