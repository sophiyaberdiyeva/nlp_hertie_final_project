
# Who Argues about What? Topic Modeling and Psychological Profiling on r/ChangeMyView

This project extends the study by Al Khatib et al. (2020) by exploring the relationship between debate topics and the psychological profiles of users on the subreddit [r/ChangeMyView](https://www.reddit.com/r/changemyview/). Using **Latent Dirichlet Allocation (LDA)** and **Linguistic Inquiry and Word Count (LIWC)**, this research identifies key thematic areas of debate and analyzes the linguistic and psychological characteristics of debaters.

## Project Overview

The internet serves as a platform for organized disagreement, with CMV being a prime example where users engage in "good faith" debates to have their minds changed. This research aims to:

1. Identify "authentic" and comprehensible thematic areas using LDA instead of simple Wikipedia categories.


2. Compare the psychological and linguistic characteristics of debaters across different topics.



## Research Questions

* 
**RQ1:** What are the main topics discussed in the r/ChangeMyView subreddit according to the LDA model? 


* 
**RQ2:** How do the psychological and linguistic characteristics of the authors of the original posts vary across different topic areas? 



## Methodology

* 
**Data Source:** The project uses the **Webis ChangeMyView Corpus 2020** (Webis-CMV-20) dataset.


* 
**Topic Modeling:** Latent Dirichlet Allocation (LDA) was implemented to extract topics from Reddit submissions.


* 
**Psychological Profiling:** LIWC2015 scores (e.g., tone, authenticity, analytic thinking) were used to profile debaters' linguistic styles and personality traits.


* 
**Analysis:** Downstream tasks include inter-topic comparisons and statistical evaluations of author characteristics.



## Main repository files

```text
├── ChangeMyView_nlp.ipynb       # Main analysis notebook (Preprocessing, LDA, LIWC analysis)
├── alkhatib.pdf					 # Main referenced paper
├── author_liwc.jsonl				 # Personality traits features computed with LIWC for the authors from pairs.jsonl dataset (from https://zenodo.org/records/3778298)
├── pairs.jsonl						 # Each record contains submission, delta-comment and nondelta-comment and the comments' similarity score (fromhttps://zenodo.org/records/3778298)
└── ds_reddit_with_topics.csv    # Processed data with assigned LDA topics
 

```

## Setup and Installation

The analysis is performed in Python. Key libraries include:

* **Data Processing:** `pandas`, `numpy`, `re`
* **NLP & Modeling:** `spacy`, `nltk`, `gensim`, `scikit-learn`
* **Visualization:** `matplotlib`, `seaborn`
* 
**Utilities:** `joblib`, `dill`, `scipy` 



To install the necessary dependencies, run:

```bash
pip install pandas numpy spacy nltk gensim scikit-learn matplotlib seaborn joblib dill scipy

```

## Key Findings

* The project successfully identified distinct topic clusters within CMV using LDA.


* Preliminary analysis revealed significant variations in linguistic markers of authors across different debate topics.



## Acknowledgments

* 
**Author:** Sofiya Berdiyeva (MDS 2024).


* 
**Course:** GRAD-E1282: Natural Language Processing at the Hertie School.


* 
**Credits:** Code was partially adapted from lab materials authored by Sascha Goebel and Luis Fernando Ramirez Ruiz.

## References

Al Khatib, K., Völske, M., Syed, S., Kolyada, N., & Stein, B. (2020). Exploiting Personal Characteristics of Debaters for Predicting Persuasiveness. In D. Jurafsky, J. Chai, N. Schluter, & J. Tetreault (Eds.), Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics (pp. 7067–7072). Association for Computational Linguistics. https://doi.org/10.18653/v1/2020.acl-main.632
