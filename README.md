# Hybrid_Deep_Learning_Smishing
Enhancing Cybersecurity: Hybrid Deep Learning Approaches to Smishing Attack Detection in Arabic Language
#  Arabic Smishing Detection using Hybrid Deep Learning
# Mohammed Rasol Al Saidat May 2025


# 📦 Prerequisites & Environment Setup for Hybrid Deep Learning Smishing Detection

Welcome to Mohammed Rasol Al Saidat Project! I created a  `Prerequisite/` directory of the **Hybrid Deep Learning Smishing Detection** project.
This guide will walk you through setting up your environment, installing required tools and dependencies, and ensuring everything is ready to run the model.
Enjoy!
---

## 🧰 Environment Specifications

| Component          | Version / Tool                      |
|--------------------|-------------------------------------|
| Python             | 3.9+                                |
| Deep Learning      | TensorFlow 2.12.0 / PyTorch (if used)|
| NLP Tools          | Gensim 4.3.0, NLTK, Farasa          |
| Model Explainability | LIME 0.2.0.1                      |
| Java (for Farasa)  | Java 8+                             |
| GPU Support        | CUDA 11.8+ and cuDNN (optional)     |

---

## 🔧 Step 1: Install Python Dependencies

If you're using `pip`:
```bash
pip install -r requirements.txt
```

Or using `conda`:
```bash
conda create -n smishing_env python=3.9
conda activate smishing_env
pip install -r requirements.txt
```

> ✅ Ensure `pip` is linked to the correct Python version (`python --version`)

---

## 📚 Step 2: Download NLTK Data

This project may require Arabic stopwords/tokenizers from NLTK:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

Alternatively, run the provided script:
```bash
python download_nltk_data.py
```

---

## 🧠 Step 3: Setup Farasa Tokenizer (Arabic NLP)

### Download Farasa Segmenter:

You must manually download the Farasa tokenizer JAR file:

```bash
bash install_farasa.sh
```

Or manually:

```bash
wget https://farasa.qcri.org/downloads/farasa-segmenter-jar-with-dependencies.jar -O farasa.jar
```

> Place it in the root or `Prerequisite/` folder

### Running Farasa from Python:

This project may use `py4j`, `subprocess`, or `os.system()` to call Farasa via Java:

```bash
java -Xmx1G -jar farasa.jar -i input.txt -o output.txt
```

If you face encoding issues, ensure the Java locale is set to UTF-8.

---

## 💾 Step 4: Word2Vec Embeddings (Optional)

You can:
- Use pre-trained Arabic Word2Vec from sources like `nlpl.eu`
- Or train your own via `train_word2vec.py`

Place trained embeddings in the following structure:

```
Word2Vec/
├── arabic_word2vec.bin
└── train_word2vec.py
```

If using pre-trained embeddings:
```bash
wget http://vectors.nlpl.eu/repository/20/52.zip
unzip 52.zip -d Word2Vec/
```

---

## ✅ Step 5: Test Your Environment

Run a forward pass or environment test script:

```bash
python test_env.py
```

Or validate GPU setup:

```python
import tensorflow as tf
print(tf.config.list_physical_devices('GPU'))
```

---

## 🧩 Optional: Using Jupyter Notebooks

You can install Jupyter and run the experiment from a notebook interface:

```bash
pip install notebook
jupyter notebook
```

---

## 🆘 Troubleshooting

| Problem                     | Solution                                      |
|----------------------------|-----------------------------------------------|
| `Java not found`           | Install Java 8+: `sudo apt install default-jdk`|
| `farasa.jar missing`       | Run `install_farasa.sh` or download manually  |
| `ModuleNotFoundError`      | Reinstall from `requirements.txt`             |
| Encoding issues (Farasa)   | Ensure UTF-8 handling on all scripts/files    |

---

## 📞 Support

For any environment issues, please contact me on mohammedrasol@gmail.com or open an issue on GitHub.

---

