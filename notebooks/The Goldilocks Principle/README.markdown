# THE GOLDILOCKS PRINCIPLE

**Key Takeaways from the paper**

- Data gathered from 108 Children's books from Project Gutenberg
- Objective : Choose answer from 10 candidate answers (single word), given a passage (20 sentences) and a question (1 sentence)
- 20 consecutive sentences are chosen from a story
- 1 word is removed from 21st sentence
- The task is to predict this one word, given the 21st sentence as question
- 10 candidates are chosen from the 21 sentences
- The candidates are of similar type
- Types of answer candidates : **NE** (Named Entity), **CN** (Common Noun), **VB** (Verb), **PE** (Preposition)

**Answer Selection from candidates**

- Refer to [Learning to Skim Text](https://arxiv.org/abs/1704.06877), Section 3.4
- The final question-aware passage representation is given by *h*o
- The best candidate has the same index that maximizes

![](bilinear.png)

- **C** - embedding matrix of 10 candidates of shape [10, d]
- *d* - embedding dimension
- **W** - output projection matrix of shape [d, hdim]
- *h*o - final representation of shape [hdim, 1]

- Section 3.4 of *Learning to Skim Text* also contains useful information for processing CBT data
