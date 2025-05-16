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

## HW5

> 2025/05/14

### 📌 Anomaly Detection and Generative Models

This assignment consists of three parts:

### 1️⃣ Abnormal Detection

* Use the **MNIST training dataset** as normal data, and a test set consisting of both **MNIST test images** and **Fashion-MNIST test images**.
* Implement the following five anomaly detection methods:

  1. **Image Classifier**: Train a classifier on MNIST and detect Fashion-MNIST images as anomalies.
  2. **Autoencoder**: Train on MNIST and use reconstruction error to detect anomalies.
  3. **Denoising Autoencoder**: Add noise during training, and use reconstruction error for anomaly detection.
  4. **Isolation Forest**: Apply directly on raw data for anomaly detection.
  5. **Pre-trained Feature Extraction + Isolation Forest**: Extract features first, then apply Isolation Forest.
* Compare the anomaly detection performance of all five methods and determine a **suitable threshold** for each.

---

### 2️⃣ Autoencoder and Variational Autoencoder (VAE)

* Select one image each of digits `0, 1, 6, 7` from the MNIST dataset, and train:

  * **Standard Autoencoder**
  * **Variational Autoencoder (latent dim = 1)**
    Compare the latent codes and reconstruction results by feeding different latent values into each decoder.

* Then, train a VAE on the full MNIST dataset with **latent dimension = 2**, and visualize:

  * (a) Using only reconstruction loss
  * (b) Using only KL divergence loss
  * (c) Using both losses together
    Observe how different loss combinations affect the latent space distribution.
    Also, discuss the potential effect on model behavior and latent space structure if the prior distribution is changed from a normal distribution to a uniform distribution.

---

### 3️⃣ Generative Models (GAN)

* Simulate two 2D data clusters centered at **(7, 7)** and **(-3, -3)**.
* Use the following generative models to learn the data distribution:

  1. **GAN / WGAN / WGAN-GP**

     * Train the model and generate 50 data points, then visualize the distribution.
  2. **InfoGAN**

     * Add a categorical input to control which cluster of data is generated.
     * Visualize how the model generates data from each cluster by manipulating the categorical variable.