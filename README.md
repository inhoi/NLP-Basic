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




