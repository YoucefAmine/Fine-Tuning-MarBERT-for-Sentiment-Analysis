# Arabic Sentiment Analysis and Text Classification (Fine Tuning MarBERT)
Sentiment Analysis is to build machine learning models that can determine the tone (positive, negative, neutral) of the texts (e.g., movie reviews, tweets...). It is one of the most important and standard tasks in NLP. However, Arabic sentiment analysis has not been studied at a level as high as other languages (e.g., English, Chinese, French...). One of the key factors is the lack of high-quality and large-scale training data.
    
- ### Datasets:
  - **[ArSAS](https://homepages.inf.ed.ac.uk/wmagdy/resources.htm)**
    - Arabic Speech-Act and Sentiment Corpus of Tweets Dataset.
    - 21K Tweets.
    - 4 Classes: Negative, Positive, Mixed and Neutral.
  - **[LABR](https://github.com/mohamedadaly/LABR)**
    - Large-Scale Arabic Book Reviews Dataset.
    - 63K Book Reviews.
    - Rating: 1 to 5.
  - **[HARD](https://github.com/elnagara/HARD-Arabic-Dataset)**
    - Hotel Arabic Reviews Dataset.
    - 94K Hotel Reviews.
    - Rating: 1 to 5.

- ### Hyper parameters:
| Parameter        | Value |
| ---------------- | ----- |
| Batch Size       | 128   |
| Optimizer        | adam  |
| Number of Epochs | 2     |

- ### Model & Results:

![Details-of-the-used-models-architecture-specifically-looking-at-one-transformer-layer](https://user-images.githubusercontent.com/45196964/215271426-4fa07ec7-dc5c-446f-b23e-68c09f2132cc.png)

**[MarBERT](https://github.com/UBC-NLP/marbert)**  is a large scale pre-training masked language model focused on both Dialectal Arabic (DA) and MSA. Arabic has multiple varieties (MarBERT use the same network architecture as AraBERT (BERT-base), but without the next sentence prediction NSP). The pre-training was done with a max sentence length of 64 only for 2 epoch. we got the following results in the table bellow

| Datasets  | **Accuracy** |
| --------- | ------------ |
| **ArSAS** | `65.35%`     |
| **LABR**  | `87.39%`     |
| **HARD**  | `96.18%`     |
