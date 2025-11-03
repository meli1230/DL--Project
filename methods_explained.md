# Machine Learning methods

## **Logistic Regression (LR)**
* **Type:** Linear model for classification.
* **How it works:** Learns weights for each feature to predict probabilities using a sigmoid (binary) or softmax (multiclass) function.
* **When used:** Strong baseline for classification tasks. Works well with small to medium datasets and when features are interpretable.

## **Support Vector Machine (SVM)**
* **Type:** Margin-based classifier.
* **How it works:** Finds a hyperplane that maximally separates classes. Uses kernel tricks (linear, RBF, polynomial) for non-linear boundaries.
* **When used:** Effective for high-dimensional data or when the dataset is not too large. Good at handling complex decision boundaries.

## **Decision Tree**
* **Type:** Tree-based, non-linear model.
* **How it works:** Splits data recursively based on feature thresholds to minimize impurity (e.g., Gini, entropy).
* **When used:** Highly interpretable and handles categorical/numeric data, but prone to overfitting.

## **Random Forest**
* **Type:** Ensemble of Decision Trees.
* **How it works:** Trains many trees on bootstrapped samples and averages their predictions.
* **When used:** More stable and accurate than a single decision tree; reduces overfitting.

## **XGBoost**
* **Type:** Gradient Boosted Trees.
* **How it works:** Builds trees sequentially where each new tree corrects the previous ones’ errors.
* **When used:** Powerful for tabular data, structured classification tasks, and competitions (Kaggle-style).



# Deep Learning methods

## **Dense Neural Network (Dense NN)**
* **Type:** Fully connected neural network (MLP).
* **How it works:** Layers of neurons connected to every neuron in the next layer; uses activations like ReLU and output softmax for classification.
* **When used:** Baseline deep model; works well with fixed-size numerical or embedding inputs.

## **Convolutional Neural Network (CNN)**
* **Type:** Spatial/pattern-based neural network.
* **How it works:** Uses convolution filters to detect local features (n-grams, edges, etc.) and pooling to aggregate them.
* **When used:** Effective for text classification (detects local patterns in embeddings) or sequence data.

## **BiLSTM (Bidirectional Long Short-Term Memory)**
* **Type:** Recurrent neural network (RNN).
* **How it works:** Processes sequences forward and backward to capture context from both directions.
* **When used:** Excellent for language or sequential data; captures dependencies between tokens.

## **BiLSTM + Attention**
* **Type:** Sequence model with a focus mechanism.
* **How it works:** The BiLSTM encodes the sequence, while attention learns which parts of the input are most relevant to each prediction.
* **When used:** Improves interpretability and performance on sequence classification tasks.


# Transformer-Based Pretrained Models

**Large pretrained models** fine-tuned for the task.

### **CodeBERT**
* **Type:** Transformer model (based on BERT) trained on **natural language + source code** (e.g., Python, Java).
* **How it works:** Learns contextual embeddings for code tokens; great for code understanding or classification tasks.
* **When used:** Semantic or syntactic classification of code snippets (e.g., functionality or category).

### **CodeT5**
* **Type:** Encoder-decoder Transformer (based on T5).
* **How it works:** Trained for multiple programming-language tasks (summarization, translation, classification).
* **When used:** Can generate or classify code; better for generation tasks and fine-tuned classification.

### **StarCoder**
* **Type:** Large language model trained on code (from the BigCode project).
* **How it works:** Autoregressive transformer model trained to predict next tokens in code sequences.
* **When used:** Great for generation, but can be fine-tuned or prompted for code classification.
