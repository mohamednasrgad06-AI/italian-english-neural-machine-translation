# 🇮🇹 Italian-English Neural Machine Translation

A neural machine translation project for translating short Italian sentences into English. The project compares a traditional **Statistical Machine Translation (SMT)** baseline with three neural sequence-to-sequence approaches:

- **LSTM Seq2Seq**
- **GRU Seq2Seq**
- **Attention-based Seq2Seq**

## 📌 Project Overview

The system receives an Italian sentence as input and generates its English translation.

Example:

```text
Italian: come stai
English: how are you
```

The project includes:

1. Data inspection and sentence-length analysis
2. SMT baseline
3. LSTM-based Seq2Seq model
4. GRU-based Seq2Seq model
5. Attention-based Seq2Seq model
6. Training and validation
7. Loss and accuracy visualization
8. Model comparison
9. Sample translation generation

## 🧠 Models

### 1. Statistical Machine Translation (SMT)

An SMT baseline was used as a traditional reference system.

Example outputs:

```text
Italian: come stai
SMT: how are you

Italian: mi piace mangiare
SMT: i like eat

Italian: buona notte
SMT: good night

Italian: dove sei
SMT: where are you
```

### 2. LSTM Seq2Seq

The LSTM model uses an encoder-decoder architecture with:

- Embedding
- Encoder LSTM
- RepeatVector
- Decoder LSTM
- Dense output layer

Training configuration:

- Epochs: 10
- Batch size: 512

Best validation results:

| Metric | Result |
|---|---:|
| Validation Accuracy | **70.61%** |
| Validation Loss | **1.7596** |

### 3. GRU Seq2Seq

The GRU model follows an encoder-decoder structure using GRU layers.

Main components:

- Embedding
- Encoder GRU
- RepeatVector
- Decoder GRU
- Dense output layer

Training configuration:

- Epochs: 10
- Batch size: 512

Best validation results:

| Metric | Result |
|---|---:|
| Validation Accuracy | **71.10%** |
| Validation Loss | **1.7323** |

### 4. Attention-based Seq2Seq

The attention model extends the encoder-decoder architecture with an **Attention** mechanism.

Architecture components include:

- Encoder input
- Decoder input
- Encoder embedding
- Decoder embedding
- Encoder LSTM
- Decoder LSTM
- Attention layer
- Concatenation layer
- Dense output layer

Training configuration:

- Epochs: 10
- Batch size: 512

Best validation results:

| Metric | Result |
|---|---:|
| Validation Accuracy | **97.41%** |
| Validation Loss | **0.2468** |

## 📊 Model Comparison

| Model | Best Validation Loss | Best Validation Accuracy |
|---|---:|---:|
| LSTM | 1.7596 | 70.61% |
| GRU | 1.7323 | 71.10% |
| **Attention Seq2Seq** | **0.2468** | **97.41%** |

### 🏆 Best Model

The **Attention-based Seq2Seq model** achieved the strongest validation performance with **97.41% validation accuracy** and **0.2468 validation loss**.

Based on the recorded validation results, it outperformed both the LSTM and GRU models.

## 📈 Training Results

The project includes training visualizations for:

- LSTM Loss and Accuracy
- GRU Loss and Accuracy
- Attention Seq2Seq Loss and Accuracy

The curves show training and validation performance across 10 epochs.

## 🔤 Translation Examples

| Italian Input | SMT | LSTM | GRU |
|---|---|---|---|
| come stai | how are you | start i you a end end | start i you it end end |
| mi piace mangiare | i like eat | start is tom end end | start i you a end end |
| buona notte | good night | start youre you end | start were you end |
| dove sei | where are you | start i you it end | start i you it end |

These examples show the generated outputs from the evaluated systems.

## 📏 Sentence Length Analysis

Sentence-length distributions were examined for both English and Italian sentences to understand the characteristics of the translation data and sequence lengths.

## 🛠️ Technologies

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook / Google Colab
- LSTM
- GRU
- Seq2Seq
- Attention Mechanism
- Statistical Machine Translation

## 📂 Project Structure

```text
italian-english-neural-machine-translation/
│
├── Italian_English_NMT.ipynb
├── README.md
│
├── assets/
│   ├── sentence_length_distribution.png
│   ├── lstm_training.png
│   ├── gru_training.png
│   ├── attention_training.png
│   ├── model_comparison.png
│   └── translation_examples.png
│
└── models/
    └── README.md
```

> The asset filenames above describe the recommended organization. Only files actually uploaded to the repository should be referenced in the final GitHub version.

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/mohamednasrgad06-AI/italian-english-neural-machine-translation.git
```

### 2. Open the notebook

Open:

```text
Italian_English_NMT.ipynb
```

using Jupyter Notebook, JupyterLab, or Google Colab.

### 3. Run the notebook

Run the cells in order to reproduce:

- Data analysis
- SMT baseline
- LSTM training
- GRU training
- Attention Seq2Seq training
- Evaluation
- Model comparison
- Translation examples

## 📌 Conclusion

The experiments show a clear difference between the evaluated approaches.

The LSTM and GRU models achieved validation accuracies of **70.61%** and **71.10%**, respectively. The Attention-based Seq2Seq model achieved **97.41% validation accuracy** with a validation loss of **0.2468**, making it the best-performing model among the evaluated approaches.

The results demonstrate the effectiveness of incorporating attention into the sequence-to-sequence translation architecture for this Italian-English translation task.

## 👤 Author

**Mohamed Nasr Gad**

GitHub: https://github.com/mohamednasrgad06-AI

## 📄 Project Notebook

The complete implementation, training process, visualizations, model architectures, and evaluation are available in:

```text
Italian_English_NMT.ipynb
```
