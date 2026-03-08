# 📖 Text Generation with RNN

> Train a model on the words of Sherlock Holmes, and it will learn to write like him. This project builds a character and word-level text generation system using Recurrent Neural Networks, trained entirely on classic Sherlock Holmes literature.

---

## 🧭 What Is This Project?

Text generation is one of the most fascinating applications of deep learning — you feed a model enough text and it starts to internalise patterns, style, and structure. This project does exactly that using an **RNN-based language model** trained on the `Sherlockbook.txt` corpus.

Multiple model variants were explored and saved — from a simple single-layer RNN to a two-layer architecture, a GloVe-enhanced version with pretrained word embeddings, and a model that hit **70% training accuracy**. Each variant reflects a different design choice, making this repo as much a learning journey as it is a finished project.

---

## 📁 Project Structure

```
Text_Generation-RNN/
│
├── Text Generation RNN Model.ipynb   # Full pipeline notebook
├── Sherlockbook.txt                  # Training corpus (Sherlock Holmes text)
├── model.h5                          # Base RNN model
├── model_2Layer.h5                   # Two-layer RNN model
├── model_70acc.h5                    # Best accuracy model (70%)
├── model_glove.h5                    # RNN model with GloVe embeddings
└── saved_model_glove_1Lay.h5         # Single-layer GloVe model
```

---

## 🛠️ Models, Concepts and Tools

**Models and Concepts:**
- 🔁 **RNN (Recurrent Neural Network)** - Learns sequential patterns in text by maintaining a hidden state across time steps
- 🧱 **LSTM / Stacked RNN Layers** - Multi-layer variant for capturing deeper language patterns and longer dependencies
- 🧬 **GloVe Embeddings** - Pretrained word vectors incorporated to give the model a head start on understanding word semantics
- 🔤 **Language Modeling** - The model learns to predict the next word/character given a sequence of previous ones
- 📉 **Temperature Sampling** - Controls how creative vs. conservative the generated text is at inference time

**Tools and Libraries:**
- 🐍 **Python** - Core language
- 📓 **Jupyter Notebook** - Development, training and experimentation
- 🤖 **TensorFlow / Keras** - Model architecture, training and saving
- 🧬 **GloVe (Global Vectors)** - Pretrained word embeddings for semantic richness
- 🔢 **NumPy** - Sequence preprocessing and data handling
- 📊 **Matplotlib** - Training curves and performance visualization

---

## 🎯 How Would a User Actually Use This?

Here's what the interaction looks like in practice. A user loads the trained model and provides a **seed text** — a short phrase or sentence to kick things off. The model then predicts the next word, appends it, and feeds the updated sequence back in, repeating this process to generate a full passage.

**Example:**

```
Seed text:  "Sherlock Holmes sat by the fire"

Generated:  "Sherlock Holmes sat by the fire and looked steadily at the paper
             which lay upon the table. I observed that his sharp eyes were fixed
             upon a small brown envelope near the corner of the mantelpiece..."
```

The model has learned the rhythm, vocabulary and narrative tone of Arthur Conan Doyle's writing. It won't always be perfect, but it will feel distinctly Holmesian — methodical, observant, Victorian in flavour.

You can also adjust the **temperature parameter** to tune the output:
- Low temperature (e.g. `0.2`) gives safe, predictable text that closely mirrors the training data
- High temperature (e.g. `1.0`) makes the model more adventurous and occasionally surprising

---

## 🌍 Real-World Applications

RNN-based text generation, while foundational, has several genuinely useful real-world applications:

- ✍️ **Creative Writing Assistance** - Writers can use it to overcome blocks by generating story continuations or dialogue in a specific author's style
- 🎮 **Game Dialogue Generation** - Games can use style-trained models to auto-generate NPC dialogue that fits the world's tone and era
- 📚 **Literary Style Transfer** - Researchers and hobbyists can train on any author's corpus to study or replicate writing styles
- 🤖 **Chatbot Prototyping** - Simple RNN models serve as baselines before scaling to Transformers in conversational AI pipelines
- 🏫 **NLP Education** - A clean, well-documented RNN text generation project is one of the best ways to learn sequence modelling hands-on
- 📰 **Content Drafting** - Domain-specific models trained on niche corpora can draft first-pass content for blogs, reports or templates

---

## 💡 Key Highlights

- **Multiple saved models** means you can directly compare outputs across architectures without retraining
- **GloVe integration** shows how pretrained embeddings improve coherence over random initialisation
- **Sherlock Holmes corpus** is a great training dataset — rich vocabulary, consistent style and long-form narrative structure
- **70% accuracy model** is saved separately so you always have the best-performing checkpoint ready to go

---

## 🙋‍♀️ About the Author

Built with 💙 by **[Pranitee Majukar](https://github.com/pranitee23)**

*If this project sparked your curiosity, a ⭐ would be wonderful!*
