# Assignment 1a Sentiment Analysis

[Open in colab](https://www.google.com)

### Pre-processing:
* Normal python coding using numpy, pandas
* Stopwords are pre-downloaded from nltk.corpus and used
* nltk.word_tokenize for tokenization
* Vocabulary is built assuming the padding (0) and unknown words(1) as tokens.       vocab["<pad>"] = 0      vocab["<unk>"] = 1
* Took the max value for padding to be 29 (largest size from train dataset given)
 
### Dataset: 
* Used pandas and sklearn.preprocessing.OneHotEncoder to get one hot representation for ratings and provided this as the target labels. 

### Softmax:
* This function is written in such a way that it handles the exploding and vanishing gradients problem. The input to softmax function is normalised by subtracting by maximum value in the input tensor and divided by reasonably big value ~10,000
### Model architecture: 
* tf.keras.Input and tf.keras.layers.Dense are used in the model architecture. 
* Used sklearn.metrics to get accuracy_score,precision_score,recall_score,f1_score,confusion_matrix

### Test results

| Metric        | Score         | 
| ------------- |:-------------:| 
| Accuracy     | 0.5783| 
| Precision      | 0.334      | 
| Recall        | 0.5783      |  
| F1-score        | 0.4238594943927011     |


