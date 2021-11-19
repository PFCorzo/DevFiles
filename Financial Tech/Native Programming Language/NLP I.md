# Intro Native Programming Language 

Natural Programming Language **([[NLP]])** are method for building computer software that understands, generates, and manipulates the human language. 

There are industries that have large quanties of textual data that can't be efficiently processed manually. For example: 
				1. Law has research, notes, documents, records of legal transactions, governmental information. 
				2. The field of medicine has patient information/history, clinical notes, symptoms.
				3. Stock market analysis has company disclosures, news articles, report narratives. 

NLP is involved in converting large text such as the one above into human readable texts. For stocks, NLPs can can read multiple text files and link the relationship between new information related to your investment, but it can also use it as parameters to suggest an investment. 

In finance, NLPs can automate [[Sentiment Analysis]] of earning statements and investor calls. Form predictions of interest rate from Federal Reserve Testimonies, create news-based indices of geopolitcal uncertainty. 

NLP is hard because humans interperet what others say(natural language) habitually/intuitively. However, a machine is not a human being; Text/words/sentences have multiple variables that can influence how the listener interprets it. Such as the context of the situation at the moment, the speakers characterstic, traits, reputation, and even the listeners own personal bias, background, culture, party affiliation. Text/words/sentences are ambiguos; meaning they can mean different things in different contexts.  Text/words/sentences are also nonstandard; meaning that through the use of grammar, syntax arrangement, etc.., can be manipulated to change the meaning of a statement.

But first, lets add some library [[Dependencies]] to our [[.env File]]: 
### Python NLP/ML/AI Environment
At an Anaconda Prompt(Logged in to your FinTech .env):
``` Bash

python -c "import nltk;nltk.download('all')"

conda install -c conda-forge wordcloud

pip install newsapi-python==0.2.5

pip install --upgrade "ibm-watson>=3.0.3"

conda install -c conda-forge spacy

python -m spacy download en_core_web_sm

conda install tensorflow

pip install finta

```


## Examples of NLP Applications

### Text Classification 
[[Text Classification]] classifies statements as subjectie/objective, positive/negative; finding the reading level or genre of a text. 

--> Input of the text 
You input the text in word, .md, Corpus, 
--> Text Classification Model 
The text classification model will begin to figure out what syntax the text contains; whether it is nouns or adjectives, are they positive or negative, is the subject being spoken of positively or negatively, are the nouns being modified, etc.,
--> Output in the form of Tags 
The program will then spin out this information in the form of tags. 

### Information Extraction
[[Information Extraction]] is the task of automatically extracting structured information from unstructured **and/or** semi-structured machine-readable documents. 

### Document Summarization 
Document summarization is implemented by extracting sentences that cover the main topics of a document with a minimum redundancy. With this you can create a tool to automatically extract the most important senteces from an article of text; it also has a physics-based network visualization of the underlying algorithm.

### Complex Question Answering 
[[Complex Question Answering]] is the ___ . Its goal is to remove the difficulty of answering questions that have multiple appositive pharase (meaning that the clause, dependent or independent, is being modified by a word or phrase). 

### 

