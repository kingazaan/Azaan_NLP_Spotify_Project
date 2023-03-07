# Azaan_NLP_Spotify_Project
A spotify text reader that plays music based on the tone of what you are reading

Step 1:

Decide your data
Knowing what text/data you want to work with is often the first and easily one of the most important steps to take. What you use may not be very obvious as there are other technical considerations. Below we are going to define the common terms associated with data in NLP fields.
Corpus: The corpus is the bulk of your text. A corpus is essentially any collection of text that you choose to analyze. 
Document: Because corpus sizes may grow huge, it is common to split corpora into documents. Documents are not necessary but for large datasets, splitting up individual topics into documents may be helpful.
Tokens: Tokens are the basic unit of measurement for NLP learning tasks. They are essentially a fancy way of saying words in the case of text documents.
Vocabulary: Like the name implies, the vocabulary of your corpus describes the tokens. For these purposes, vocabulary will be the number of distinct tokens within your corpus.
We recommend for now to use datasets that are well-made and logical. By logical, we mean that it is very obvious how your vocabulary scales with your corpus size. For example, a corpus may increase linearly, but the vocabulary scales logarithmically. Knowing these factors will help you greatly in deciding a good size split. 
Data Extraction/Processing
Raw data is useless for us. We need to find a way to extract meaningful data and process it so that is clear and concise. 
Extraction: Extraction is a fairly simple process that does not require much on your end. Simply use an available tool and let it extract all the data for you. For example, Spacy is a common tool to extract text data into usable tokens.
Processing: Processing is the step that is much more subjective. Similar to extraction, we have to first attain the tokens that a model can use. Likewise, we need to format the data in a way that makes it readable for the model. For example, one part that you might want to focus on is model indexing i.e. what list do you want your model to be indexed on. 

Step 2:
Algorithms
Choosing your algorithm for NLP projects is not a plug-and-chug system. By algorithms, we mean what process you want to use on your data to get a meaningful result. This could be converting text to numbers to perform some form of similarity calculation. This could also be a Bag of Words approach to determine tags of certain sentences. Depending on your project, your “algorithm” is what you want to use to achieve your goal.
Neural Networks/Models
We will likely have a form of model or neural network to generate our predictions. We will not specify much on this step as there are many many resources online on choosing the best model/neural network for your problem. There is a high level of abstraction for these tools, so it is absolutely not necessary to completely understand the model to use it.
Evaluation
The evaluation step is the final step of your project. Now that everything has been processed and put through a model/network, all that is left is to see the performance. There are many ways to evaluate the model performance and most will likely be enough for your models. If your evaluation is not very high, backtrack and see what you can change. This will likely be replacing your “algorithm” or model.

Vectorizing Words

Possible Usecases: Word Similarity Analysis, Paraphrasing, Summarizer, Plagiarism Detector, Autocorrect/Autofill

# Based on the implementation found at https://stackoverflow.com/a/8897648

from sklearn.feature_extraction.text import TfidfVectorizer

text_files = ‘[YOURTEXT].txt', [YOURTEXT].txt’ ']
documents = [open(f, encoding="utf8").read() for f in text_files]
tfidf = TfidfVectorizer().fit_transform(documents)  # returns normalized vectors 
pairwise_similarity = (tfidf * tfidf.T).A
#print(pairwise_similarity)

Also check out Word2Vec from GenSim
*For implementation check out last year's SIGNLLtle game
https://github.com/SIGNLL-UIUC/SIGNLLtle

Tokenizing words as vectors is a very common method used within NLP. Computers are used to operating numerically. Vectorizing words is a super powerful tool that allows you to make comparisons that would otherwise not be intuitive.