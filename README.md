# Pre-trained word vectors for Vietnamese

This project contains embedding for 437,485 Vietnamese unique words from a corpus of 93,546 top documents from Vietnamese Wikipedia. Note that all words are tokenized words.

## Requirements
* gensim > =0.13.1 (for Word2Vec)
* pyvi (for word tokenizer)
<!--* fastText (for [fasttext](https://github.com/facebookresearch/fastText))-->
	
## Background / References
* Check [this](https://en.wikipedia.org/wiki/Word_embedding) to know what word embedding is.
* Check [this](https://en.wikipedia.org/wiki/Word2vec) to quickly get a picture of Word2vec.
<!--* Check [this](https://github.com/facebookresearch/fastText) to install fastText.-->

## Pre-trained models
Download the [ML4U vi embedding](https://drive.google.com/open?id=1-6amAqdYfJm-VkR0FBOLVelro5J0TJpE).

## Example

```
In[0]: 
from gensim import models
words = models.KeyedVectors.load_word2vec_format('ML4U_QA_embed.txt', binary=False)
words.most_similar('vua')

Out[5]: 
[('hoàng_đế', 0.8315562009811401),
('quốc_vương', 0.7650110721588135),
('pharaon', 0.699152410030365),
('hoàng_hậu', 0.6941052675247192),
('khalip', 0.6764698028564453),
('hoàng_tử', 0.6755297183990479),
('hoàng_thân', 0.6730912923812866),
('chư_hầu', 0.6716309785842896),
('thái_tử', 0.6599626541137695),
('danh_tướng', 0.6498899459838867)]
```
