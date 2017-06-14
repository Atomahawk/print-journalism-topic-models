Python  | Numpy | Pandas | Statsmodels | Sci-Kit Learn
--------|-----|-----|---------|------
[![PyPI](https://img.shields.io/badge/python-3.5-blue.svg)]() | [![PyPI version](https://badge.fury.io/py/numpy.svg)](https://badge.fury.io/py/numpy) | [![PyPI version](https://badge.fury.io/py/pandas.svg)](https://badge.fury.io/py/pandas) | [![PyPI version](https://badge.fury.io/py/statsmodels.svg)](https://badge.fury.io/py/statsmodels) |  [![PyPI version](https://badge.fury.io/py/scikit-learn.svg)](https://badge.fury.io/py/scikit-learn)

Repo update in progress! Slides live [here](https://docs.google.com/presentation/d/1EsK5ZUHGKwBlq2QcCHTk0cNmycLwj96eaILlKTLJFnQ/edit?usp=sharing).  **Code coming soon**

# Print Journalism Article Classifier and Topic Models

- Unsupervised topic modeling of print journalism corpora ranging from tabloid articles to broadsheet articles.
- Trained a classifier to distinguish between tabloid and broadsheet articles based off the language provided.

## Problem Statement
What’s driving sensationalist news is a change in the fundamental business model of news reporting: from a few well fact-checked news agencies to the new internet enabled anyone-can-write-a-headline-and-get-paid free for all.
- There are lots of us who understand the inherent danger in the proliferation of sensationalist news without substance or depth.
- I wanted to demonstrate using data science and objective measuring as a potential check on accurate and fair reporting within journalism.

**Problem: Illustrate distinctions between broadsheet and tabloid journalism.**

#### On Motives for Filtering News
- I believe improving civil discourse begins with more consumption of news with substance or depth.
- Although I could not assess an article's content for truth-value in an automated way, I could use NLP to objective measure word style and language choice to make clear distinctions to measure 'sensationalist' stories relative to my training set.

## Data measuring the difference between broadsheets and tabloids

Broadsheets have come to be associated with a high-minded approach to the dissemination of news, and with an upscale readership. Even today, broadsheet papers tend to employ a traditional approach to newsgathering that emphasizes in-depth coverage and a sober tone in articles and editorials.

** Broadsheet training examples:  NYT, Reuters, Associated Press **
 - Justification: The Times has been an annual winner of Pulitzer Prizes, and has so far amassed 117 of them, beginning in 1918 for its coverage of World War I. The Times is one of the few newspapers that has been successful in monetizing the Internet because it is so well-known and well-respected worldwide that people are willing to pay a subscription fee to read it online. 
- Pulled a corpus of 10,000+ documents from NYT API.


In contrast, tabloids tend to be more irreverent and slangy in their writing style than their more serious broadsheet brothers. In a crime story, a broadsheet might refer to a police officer, while the tabloid will call him a cop. And while a broadsheet might spend dozens of column inches on "serious" news - say, a major bill being debated in Congress - a tabloid is more likely to zero in on a heinous sensational crime story or celebrity gossip.

** Tabloid training examples: http://www.opensources.co/ **
- Justification: Trusting on the integrity of university affiliated academics, I scraped a corpus 6000+ documents of **click-bait** news articles from many of the sources provided.


## Analytical Approach

Will better explain the questions guiding analyses and a summary of the methods involved.

- TF-IDF Vectorizer --> Multinomial Naive Bayes Classifier
- CountVectorizer --> HDP --> LDA --> Clustering & Topic Modeling


## Tool Stack

- AWS t2.medium linux EC2 instance with a MongoDB database
- Jupyter notebook
- Python 3.5
- [Newspaper](https://github.com/codelucas/newspaper/), BeautifulSoup4
- Sci-kit Learn
- NLTK
- Gensim
- D3.js

Might include step by step series of examples that tell you have to get a development env running

## Visuals [In Development]
- See slide deck.  Interactive word clouds coming soon.


## Conclusions
More to come.  Will explain insights gleaned, model evaluation, or patterns in visualization.

Best Performer: Multinomial Naive Bayes Classifier
- Score: 95%

```
Give an example
```

## Future Work

Expand to other aspects of fake news as described by Brennan Borlaug - one member of small team of grad students at UC Berkeley who have defined 'fake news' as a broad category of the following attributes:
- Clickbait — Shocking headlines meant to generate clicks to increase ad revenue. Oftentimes these stories are highly exaggerated or totally false.
- Propaganda — Intentionally misleading or deceptive articles meant to promote the author’s agenda. Oftentimes the rhetoric is hateful and incendiary.
- Commentary/Opinion — Biased reactions to current events. These articles oftentimes tell the reader how to perceive recent events.
- Humor/Satire — Articles written for entertainment. These stories are not meant to be taken seriously.


## Author

* [**Andrew Tom**](https://github.com/Atomahawk)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments & Inspirations

* Credit to Melissa Zimdars of Merrimack College and her research team for the clickbait-y news sources: http://www.opensources.co/
* Udemy Course: [Dan Rather On Journalism and Integrity in the News](https://docs.google.com/document/d/1UVVm6Ic0m5842JjSAJCTwutLp-K0dD7f-wtblHAN3rA/edit#heading=h.agfnahz97djy)
* 2016 Election Cycle: https://www.martechadvisor.com/articles/content-marketing/the-misinformation-age-ais-role-in-recognizing-fake-news/

