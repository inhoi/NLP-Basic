# NLP-Basic

## Text Cleaning
1. Converting to lowercase
2. Removing URLs
3. Removing non-word and non-whitespace chars
4. Removing digits
## Tokenization
- Breaking down large blocks of text into smaller, managable units
  
![image](https://github.com/inhoi/NLP-Basic/assets/76868046/6d9f7c0e-612d-4bb8-9870-59bb0960eb89)

## Removing Stopwords
- Mostly common occurring words in any natural language
- Help to focus on most important information in text
- Reduce size of dataset
  
![image](https://github.com/inhoi/NLP-Basic/assets/76868046/5422b537-aa8d-405a-ae7a-07d697be91ec)

## Stemming
- Cutting off ends of words and obtaining correct root form
- automate, automatic, automation --> automat
  
## Lemmatization
- Remove inflectional endings only and return base or dictionary form of word
- car, cars, cars', car's --> car
- am, is, are --> be


## Word Cloud
- Help analyze large texts to highlight essesntial parts and find main messages
- Allow comparing two different pieces of text, find similarities

![image](https://github.com/inhoi/NLP-Basic/assets/76868046/084d7e2d-4b5c-4db3-9b92-4772a9a0485a)

## N-Grams
- Continuous sequences of words or tokens in document
- n=1 --> Unigram
- n=2 --> Bigram
- n=3 --> Trigram

ex) I like to play soccer

| SL.No. | 	Type of n-gram	 |    Generated n-grams |
| :---: | :---: | :---: |
| 1	| Unigram |	“I”, ”like”, ”to”, ”play”, "soccer"|
| 2 | 	Bigram	| “I like”, ”like to”, ”to play”, "play soccer"|
| 3 | 	Trigram |	“I like to”,  “like to play”, "to play soccer" |

ex) I like to eat and like to play ___?___

like to play -- 1000

like to play soccer -- 500

like to play baseball -- 200

$$ P(w\text{|like to play}) = \frac{\text{count(like to play}\ w)}{\text{count(like to play)}} $$

$$ P(\text{soccer|like to play}) = 0.500 $$

$$ P(\text{baseball|like to play}) = 0.200 $$

## TF-IDF (Term Frequency - Inverse Document Frequency)
- Calculation of how relevant word in series or corpus is to a text
- Meaning increases proportionally to the number of times in the text a word appears but is compensated by the word frequency in the corpus

$$ tf(t, d) = \frac{\text{count of term } t \text{ in document } d}{\text{number of words in document } d} $$     

$$ idf(t) = \log_2 \left( \frac{N}{df(t)} \right) $$      

$$ tf-idf(t, d) = tf(t, d) \cdot idf(t) $$

- TF is the term frequency of a word in a document ( between 0 and 1 ),  IDf ( >= 0) 
- N is the total number of documents in the corpus
- DF is the document frequency of a word in the corpus (i.e., the number of documents that contain the word)

ex)

Doc1: The quick brown fox jumps over the lazy dog  

Doc2: The lazy dog likes to sleep all day 

Doc3: The brown fox prefers to eat cheese 

Doc4: The red fox jumps over the brown fox

Doc5: The brown dog chases the fox


- Step 1 : Calculate the term frequency (TF)
- 
  
TF = (Number of times word appears in the document) / (Total number of words in the document)

Doc1: 1 / 9

Doc2: 0 / 8

Doc3: 1 / 7

Doc4: 2 / 8

Doc5: 1 / 6


- Step 2 : Calculate the document frequency (DF)

DF = 4 (Doc1, Doc3, Doc4 and Doc5)


- Step 3: Calculate the inverse document frequency (IDF)

IDF = log(5/4) = 0.2231


- Step 4: Calculate the TF-IDF score

TF-IDF = TF * IDF

Doc1: 1/9 * 0.2231 = 0.0247

Doc2: 0/8 * 0.2231 = 0

Doc3: 1/7 * 0.2231 = 0.0318

Doc4: 2/8 * 0.2231 = 0.0557

Doc5: 1/6 * 0.2231 = 0.0372







