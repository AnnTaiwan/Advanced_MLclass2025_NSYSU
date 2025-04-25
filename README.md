# NSYSU ADV_ML 2025 HW 
## HW1
* Analyze `datasets.make_circles` distribution by pytorch model.
## HW2
* Dataset: MNIST
* Target: Train an CNN model to predict the digit number in given dataset.
* Make model as small as possible. 
## HW3 
### 1. Develop RNN models to classify the images. (**Same as HW2**)
* Dataset: MNIST
* Target: Train the SimpleRNN, LSTM and GRU model to predict the digit number in given dataset.
### 2. Deal with the text data, and learn how to embedd them.
* Dataset: HW3_ text.csv
#### 2.1. Develop two models to classify these texts into one of the three possible sentiments.
#### 2.2. Develop an RNN model that can predict the remaining words of a sentence based on the initial words you input.

## HW4 
>2025/04/26
### 1. Utilize the `CLIP` model to perform image classification (Do **zero-shot**)
### 2. Fine-tune the `BERT` model.
### 3. Demonstrate the derivation of the total number of parameters (weights) in the LLaMA2-7B model. (Note: LLaMA2-7B uses the grouped-query attention mechanism—please take this into account in your calculation.)
### 4. Utilize the `ChromaDB`, and I perform on a movie dataset.
### 5. Develop a Python program that accepts an image and a textual description, and determines whether the content of the image matches the description. Report whether the match is valid or not.
* I use the same `CLIP` model as `1`, while I test **zero-shot** on `CIFAR100` dataset in order to see if the match is valid or not (see **top-1 accuracy**).