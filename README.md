# semantic_space_and_size

this project is an extension of the [Word Embedding Association Test (WEAT)](https://arxiv.org/abs/1608.07187) framework, proposed in 2016 by Caliskan et al.

includes code to scrape more than a dozen subReddits, obtaining roughly 111,000 tokens for linguistic research, creating more than a dozen corpora with a mean unique vocabulary of 5,580 tokens exclusive of stop-words. automated text preprocessing to obtain top n-grams, train 18 unique Word2Vec neural networks for shallow neural vectorization, & automate scalable in-depth cosine similarity analysis. callable in one line of Python.

## about WEAT

the WEAT test was based on the discovery that word embeddings also encoded measureable social biases, which correlated to known cultural phenomena:

*Our results indicate that language itself contains recoverable and accurate imprints of our historic biases, whether these are morally neutral as towards insects or flowers, problematic as towards race or gender, or even simply veridical, reflecting the {\em status quo} for the distribution of gender with respect to careers or first names. These regularities are captured by machine learning along with the rest of semantics. In addition to our empirical findings concerning language, we also contribute new methods for evaluating bias in text...*

the paper speculated that the test could be applied to study historical cultures via vectorization & cosine similarity analysis of their surviving corpora, provided the corpora were large enough--however, historical corpora are notoriously limited, and the paper gave no guidance as to what size might be technically feasible given the constraints of shallow word embeddings.

this project aims to answer that question, as a proof-of-concept for applying WEAT analysis on *very* small corpora.

while the original paper used `GloVe` word embeddings trained on the Common Crawl (a very large corpus), this project uses the `Word2Vec` algorithm, trained on individual subreddits selected for their relatively small size (20,000 tokens or fewer) and ease of testing biases. for more information on `Word2Vec`, see [this blog post](https://towardsdatascience.com/word2vec-explained-49c52b4ccb71).

in addition to `Word2Vec` from `gensim`, this project also makes use of the `praw`, `nltk`, `sklearn` and `matplotlib` libraries.

code for this project lives in [a jupyter notebooke here](https://anglesofattack.io/3/semantic_space_and_size.html). find the [full writeup with results here](https://github.com/disesdi/semantic_space_and_size/blob/fd2583ae637447ef383f6011531f79eae481b6a5/small_corpora_bias_analysis_1.ipynb).
