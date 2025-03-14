TextAnalyzer
TextAnalyzer is a Flask-based web application that provides various NLP (Natural Language Processing) features for text analysis, including sentiment analysis, keyword extraction, named entity recognition (NER), text statistics, and spelling correction. The application uses multiple NLP libraries such as SpaCy, NLTK, and VaderSentiment, along with machine learning techniques to enhance the functionality.

Table of Contents
Technologies Used
Installation
Usage
Features
License
Technologies Used
Flask - A web framework for Python that powers the app's backend.
SpaCy - For Named Entity Recognition (NER) and other NLP tasks.
NLTK - For text tokenization and sentence segmentation.
VaderSentiment - For sentiment analysis.
RAKE - For keyword extraction.
LanguageTool - For grammar and spelling checks.
PyEnchant - For enhanced spelling correction.
Matplotlib - For visualizing sentiment analysis and text statistics.
SpellChecker - For spelling correction.
Installation
To run the TextAnalyzer locally, follow these steps:

1. Clone the repository
bash
git clone https://github.com/yourusername/TextAnalyzer.git
cd TextAnalyzer
2. Create a virtual environment (optional but recommended)
bash
python -m venv venv
3. Activate the virtual environment
Windows
bash
.\venv\Scripts\activate
Mac/Linux
bash
source venv/bin/activate
4. Install required libraries
bash
pip install -r requirements.txt
The requirements.txt file should contain the following libraries (add them if missing):

txt
Flask==2.0.1
spacy==3.0.6
nltk==3.6.3
vaderSentiment==3.3.2
rake-nltk==1.0.4
language_tool_python==2.0.0
pyenchant==3.2.1
matplotlib==3.4.3
SpellChecker==0.6
5. Download the required NLTK data
The app requires certain NLTK data files to be downloaded. Run the following in Python:

python
import nltk
nltk.download('punkt')
6. Install the SpaCy language model
To enable Named Entity Recognition (NER) with SpaCy, download the English model:

bash
python -m spacy download en_core_web_sm
Usage
After setting up the environment and installing dependencies, you can start the Flask application by running the following command:
bash
python app.py
Open your browser and go to http://127.0.0.1:5000/ to access the web application.

On the homepage, you can input any text to be analyzed. Upon submission, the following features will be displayed:

Original Text
Preprocessed Text
Sentiment Analysis (with a visual representation)
Keyword Extraction
Named Entity Recognition (NER)
Text Statistics
Spelling Correction
Features
Sentiment Analysis: Uses the VaderSentiment library to determine if the input text is positive, negative, or neutral, and provides a sentiment score.
Keyword Extraction: Utilizes RAKE (Rapid Automatic Keyword Extraction) to identify the top 5 keywords from the text.
Named Entity Recognition (NER): Extracts named entities like person names, organizations, locations, and more using SpaCy.
Text Statistics: Provides basic statistics on the input text such as character count (with and without spaces), word count, and sentence count.
Spelling Correction: Corrects spelling mistakes using pyEnchant, SpellChecker, and LanguageTool for both spelling and grammar issues.
Visualization: Displays charts for sentiment analysis and text statistics using Matplotlib.
