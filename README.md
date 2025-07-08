# 🧙‍♂️ Chandler Bing Meets Hogwarts: A Fine-Tuned RAG System

> What if Chandler Bing had read *Harry Potter* and answered your questions — with sarcasm, wit, and just a dash of wizardry?

This project brings together modern Retrieval-Augmented Generation (RAG), fine-tuned LLMs, and humor — to create a **Chandler Bing-styled chatbot** trained on the *first 5 Harry Potter books*. Built with a full-stack AI pipeline from embeddings to model fine-tuning and RAG orchestration.

---

## 🧩 Project Overview

This repo showcases a complete workflow that combines:

- 📚 Embedding of long-form documents (*first 5 Harry Potter books*)
- 🤖 RAG-based retrieval using `ChromaDB`, `Docling`, and `Gemma`
- 🧠 Custom dataset generation using `Ollama` with **prompt-stylized Q&A**
- 🎭 Fine-tuning `LLaMA 3.1B Instruct` to mimic **Chandler Bing's voice**
- 🌐 Serving through a Chandler-finetuned model in `Ollama`
- ⚙️ Full Colab-compatible pipeline and step-by-step code for replication

---

## 🔥 Live Demo Model

> 🔗 [ChandlerBing-Potterhead-Llama-3.1B-Instruct on Ollama](https://ollama.com/kapooradit/ChandlerBing-Potterhead-Llama-3.1B-Instruct)

---

## 🧠 Tech Stack Breakdown

| Layer               | Tool / Library |
|---------------------|----------------|
| **LLM Backbone**     | `LLaMA 3.1B Instruct` (Meta) |
| **Fine-Tuning**      | `LoRA`, `Transformers`, `trl`, `Colab` |
| **Data Retrieval**   | `Docling`, `ChromaDB` |
| **Embeddings**       | `Gemma`, HuggingFace embeddings |
| **Prompting & Dataset Generation** | `Ollama`, custom prompt templates |
| **RAG Logic**        | Custom Python logic with document search + LLM |
| **Deployment**       | `Ollama` (local/hosted) |
| **Dev Tools**        | `Google Colab`, `VS Code`, `GitHub` |

---

## 🛠️ Architecture Flow

```plaintext
1. Harry Potter Books (Books 1–5)
       |
       v
2. Text Chunking + Embeddings (Docling + Gemma)
       |
       v
3. Stored in ChromaDB as vector DB
       |
       v
4. ~400+ Qs auto-generated
       |
       v
5. Each Q retrieved context → sent to Ollama
       |                           |
       |--> Prompted for Chandler-style answer
       |
       v
6. Dataset = (Q, context, Chandler-style answer)
       |
       v
7. Fine-tune LLaMA 3.1B with TRL + LoRA
       |
       v
8. Upload to Ollama as:
   👉 `ChandlerBing-Potterhead-Llama-3.1B-Instruct`
       |
       v
9. Final RAG Pipeline:
   Embed books → retrieve → Chandler responds
