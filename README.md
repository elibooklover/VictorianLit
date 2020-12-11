# VictorianLit

VictorianLit Dataset for Machine Learning-Based Sentiment Analysis of Victorian Literary Texts | by Hoyeol Kim

---
### Download: [VictorianLit (Kaggle)](https://www.kaggle.com/elibooklover/victorianlit/download)

##### You can download the VictorainLit dataset directly by using the following URL: 
```
https://elibooklover.github.io/VictorianLit/VictorianLit.csv
```
Here is example code for loading the VictorianLit dataset: 
```
df=pd.read_csv('https://elibooklover.github.io/VictorianLit/VictorianLit.csv')
df.head()
```
---
### Dataset
There are two columns: sentences and label. The VictorianLit dataset has five labels based on sentiment: 0 (very negative), 1 (negative), 2 (neutral), 3 (positive), 4 (very positive).

The VictorianLit dataset, which has 53,826 rows and 2 columns, consists of five different novels from the Victorian era: Charles Dickens' *Little Dorrit* and *Oliver Twist*, Elizabeth Gaskell's *North and South*, George Eliot's *Adam Bede*, and Mary Elizabeth Braddon's *Lady Audley's Secret*. The maximum sentence length of the VictorianLit dataset is 372.

![VictorianLit1](https://elibooklover.github.io/VictorianLit/VictorianLit1.png)

![VictorianLit2](https://elibooklover.github.io/VictorianLit/VictorianLit2.png)

![VictorianLit3](https://elibooklover.github.io/VictorianLit/VictorianLit3.png)

---
### Test Results
The VictorianLit dataset was tested with the [BERT-Base](https://github.com/google-research/bert) model released by [Google Research](https://github.com/google-research). The BERT-Base, Uncased model (12-layer, 768-hidden, 12-heads, 100M parameters) was run with the VictorianLit dataset in order to validate the dataset.

For fine-tuning BERT for sentiment analysis, the following hyperparameters and training environments were set:

* tokenizer: BertTokenizer
* max_sequence_length: 400
* batch_size: 16
* model_name: BERT-base, Uncased (12-layer, 768-hidden, 12-heads, 110M parameters)
* learning_rate: 1e-5
* epochs: 4
* GPU: Tesla T4

The accuracy is 93%, and the average training loss is 0.12. If the batch_size was larger, the accuracy would be higher. If your GPU ram is enough to cover the large batch_size, I recommend you set the batch_size to 64 or 128.

---
### Feedback
The VictorianLit dataset will be continuously updated, added upon, and tested. Please feel free to provide any feedback or suggest sentiment value changes with supporting statements.

---
### Citation
Please use the following reference to cite the dataset:
```
@misc{VictorianLit,
    author       = {Hoyeol Kim},
    title        = {{VictorianLit Dataset for Machine Learning-Based Sentiment Analysis of Victorian Literary Texts}},
    month        = Sep,
    year         = 2020,
    publisher    = {GitHub},
    url          = {https://github.com/elibooklover/VictorianLit}
    }
```

or 

```
Kim, Hoyeol, VictorianLit Dataset for Machine Learning-Based Sentiment Analysis of Victorian Literary Texts, September 2020. GitHub repository: github.com/elibooklover/VictorianLit.
```
---
[License](https://creativecommons.org/licenses/by-nc-sa/4.0/)

![License](https://elibooklover.github.io/VictorianLit/license.png)
