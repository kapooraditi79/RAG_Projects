# 🧙‍♂️ Chandler Bing Meets Hogwarts: A Fine-Tuned RAG System

> What if Chandler Bing had read *Harry Potter* and answered your questions — with sarcasm, wit, and just a dash of wizardry?

A fine-tuned Retrieval-Augmented Generation (RAG) system that combines Harry Potter knowledge with Chandler Bing's witty personality from the TV show "Friends". This project demonstrates advanced NLP techniques including document processing, vector embeddings, dataset generation, model fine-tuning, and RAG implementation.
---

## 🎯 Project Overview

This project creates a unique conversational AI that answers Harry Potter-related questions in Chandler Bing's distinctive sarcastic and humorous style. The system leverages a multi-stage pipeline:

1. **Initial RAG Pipeline** : Built with Docling, ChromaDB, Gemma, and text embedding models using the first 5 Harry Potter novels
2. **Dataset Generation** : Created 400+ questions and answers in Chandler Bing's style using Ollama
3. **Model Fine-tuning** : Fine-tuned Llama 3.1 8B Instruct model on the generated dataset
4. **Final RAG System** : Integrated the fine-tuned model with document retrieval for enhanced responses

---

## 🔥 Live Demo Model

> 🔗 [ChandlerBing-Potterhead-Llama-3.1B-Instruct on Ollama](https://ollama.com/kapooradit/ChandlerBing-Potterhead-Llama-3.1B-Instruct)

---

## 🛠️ Tech Stack

## Core Technologies

* **Document Processing** : Docling for PDF parsing and text extraction
* **Vector Database** : ChromaDB for storing and retrieving document embeddings[1](https://github.com/rupeshtr78/chroma-db-rag)[2](https://realpython.com/chromadb-vector-database/)
* **Embedding Models** : Text embedding models for semantic search
* **Language Models** :
* Gemma for initial RAG implementation
* Llama 3.1 8B Instruct for fine-tuning[3](https://www.koyeb.com/tutorials/fine-tune-llama-3-1-8b-using-qlora-koyeb-serverless-gpus)[4](https://aws.amazon.com/blogs/machine-learning/fine-tune-meta-llama-3-1-models-for-generative-ai-inference-using-amazon-sagemaker-jumpstart/)[5](https://huggingface.co/blog/mlabonne/sft-llama3)
* **Model Serving** : Ollama for hosting and serving the fine-tuned model
* **Development Environment** : Google Colab
* **Version Control** : Git with VS Code for repository management[6](https://graphite.dev/guides/how-to-push-code-from-vscode-to-github)

## Key Libraries & Frameworks

* **Vector Operations** : ChromaDB for efficient similarity search[1](https://github.com/rupeshtr78/chroma-db-rag)[2](https://realpython.com/chromadb-vector-database/)
* **Model Fine-tuning** : QLoRA technique for efficient training[3](https://www.koyeb.com/tutorials/fine-tune-llama-3-1-8b-using-qlora-koyeb-serverless-gpus)[4](https://aws.amazon.com/blogs/machine-learning/fine-tune-meta-llama-3-1-models-for-generative-ai-inference-using-amazon-sagemaker-jumpstart/)
* **Text Processing** : Various NLP libraries for document chunking and preprocessing
* **Model Conversion** : Tools for GGUF format conversion[7](https://www.geeksforgeeks.org/machine-learning/how-to-convert-any-huggingface-model-to-gguf-file-format/)[8](https://blog.devgenius.io/transpose-huggingface-models-to-gguf-format-6071c86ad2cc)

## 📁 Project Structure

<pre class="not-prose w-full rounded font-mono text-sm font-extralight"><div class="codeWrapper text-textMainDark selection:text-super selection:bg-super/10 bg-offset dark:bg-offsetDark my-md relative flex flex-col rounded font-mono text-sm font-thin"><div class="translate-y-xs -translate-x-xs bottom-xl mb-xl sticky top-0 flex h-0 items-start justify-end"><button data-testid="copy-code-button" type="button" class="focus-visible:bg-offsetPlus dark:focus-visible:bg-offsetPlusDark hover:bg-offsetPlus text-textOff dark:text-textOffDark hover:text-textMain dark:hover:bg-offsetPlusDark dark:hover:text-textMainDark font-sans focus:outline-none outline-none outline-transparent transition duration-300 ease-out font-sans  select-none items-center relative group/button  justify-center text-center items-center rounded-full cursor-pointer active:scale-[0.97] active:duration-150 active:ease-outExpo origin-center whitespace-nowrap inline-flex text-sm h-8 aspect-square"><div class="flex items-center min-w-0 font-medium gap-1.5 justify-center"><div class="flex shrink-0 items-center justify-center size-4"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7999999999999998" stroke-linecap="round" stroke-linejoin="round" class="tabler-icon tabler-icon-copy "><path d="M7 7m0 2.667a2.667 2.667 0 0 1 2.667 -2.667h8.666a2.667 2.667 0 0 1 2.667 2.667v8.666a2.667 2.667 0 0 1 -2.667 2.667h-8.666a2.667 2.667 0 0 1 -2.667 -2.667z"></path><path d="M4.012 16.737a2.005 2.005 0 0 1 -1.012 -1.737v-10c0 -1.1 .9 -2 2 -2h10c.75 0 1.158 .385 1.5 1"></path></svg></div></div></button></div><div class="-mt-xl"><div><div data-testid="code-language-indicator" class="text-text-200 bg-background-300 py-xs px-sm inline-block rounded-br rounded-tl-[3px] font-thin">text</div></div><div class="pr-lg"><span><code><span><span>bing_finetuned/
</span></span><span>├── ChandlerBingFineTuned_Final.ipynb    # Model fine-tuning implementation
</span><span>├── RAGSystemAndDatasetBuilt_final.ipynb # RAG pipeline and dataset generation
</span><span>├── ChandlerRAGSystem.ipynb              # Final RAG system with fine-tuned model
</span><span>└── README.md                            # This file
</span><span></span></code></span></div></div></div></pre>

## 🚀 Implementation Pipeline

## Stage 1: Initial RAG System

* **Document Processing** : Used Docling to extract and process text from the first 5 Harry Potter novels
* **Vector Embeddings** : Created embeddings using text embedding models
* **Vector Storage** : Stored embeddings in ChromaDB for efficient retrieval[1](https://github.com/rupeshtr78/chroma-db-rag)[2](https://realpython.com/chromadb-vector-database/)
* **Base Model** : Implemented initial RAG using Gemma model

## Stage 2: Dataset Generation

* **Question Generation** : Created 400+ questions related to the first 5 Harry Potter books
* **Style Transfer** : Used Ollama with custom prompts to generate answers in Chandler Bing's witty, sarcastic style
* **Dataset Compilation** : Stored question-answer pairs for model training

## Stage 3: Model Fine-tuning

* **Base Model** : Llama 3.1 8B Instruct model[3](https://www.koyeb.com/tutorials/fine-tune-llama-3-1-8b-using-qlora-koyeb-serverless-gpus)[4](https://aws.amazon.com/blogs/machine-learning/fine-tune-meta-llama-3-1-models-for-generative-ai-inference-using-amazon-sagemaker-jumpstart/)[5](https://huggingface.co/blog/mlabonne/sft-llama3)
* **Fine-tuning Technique** : Applied QLoRA for efficient training[3](https://www.koyeb.com/tutorials/fine-tune-llama-3-1-8b-using-qlora-koyeb-serverless-gpus)[4](https://aws.amazon.com/blogs/machine-learning/fine-tune-meta-llama-3-1-models-for-generative-ai-inference-using-amazon-sagemaker-jumpstart/)
* **Training Data** : Custom dataset with Chandler Bing-style responses about Harry Potter
* **Model Hosting** : Deployed fine-tuned model on Ollama platform

## Stage 4: Final RAG Integration

* **Document Retrieval** : Maintained ChromaDB embeddings for the 5 novels
* **Enhanced Generation** : Integrated fine-tuned Chandler Bing model for response generation
* **Complete Pipeline** : Combined retrieval and generation for contextually accurate, personality-driven responses

## 🎭 Fine-tuned Model

The fine-tuned model is available on Ollama:

 **Model** : [kapooradit/ChandlerBing-Potterhead-Llama-3.1B-Instruct](https://ollama.com/kapooradit/ChandlerBing-Potterhead-Llama-3.1B-Instruct)

## Model Conversion Note

The original GGUF file has been removed from the repository due to GitHub's file size limitations. If you need to convert your own model to GGUF format, refer to this comprehensive guide: [How to convert any HuggingFace Model to gguf file format](https://www.geeksforgeeks.org/machine-learning/how-to-convert-any-huggingface-model-to-gguf-file-format/)[7](https://www.geeksforgeeks.org/machine-learning/how-to-convert-any-huggingface-model-to-gguf-file-format/).

## 💻 Development Environment

## Google Colab Implementation

* **Primary Development** : All code was initially developed and tested in Google Colab
* **GPU Utilization** : Leveraged Colab's GPU resources for model training and inference
* **Collaboration Features** : Used Colab's collaborative environment for iterative development

## Repository Management

Due to Colab's state management limitations, the code was transferred to GitHub through the following process:

1. **Local Download** : Downloaded individual notebook files from Colab
2. **VS Code Integration** : Used VS Code for final code organization and repository management[6](https://graphite.dev/guides/how-to-push-code-from-vscode-to-github)
3. **Git Operations** : Performed version control operations through VS Code's integrated Git interface[6](https://graphite.dev/guides/how-to-push-code-from-vscode-to-github)[9](https://stackoverflow.com/questions/46175462/vs-code-git-push-is-not-pushing-the-code-to-remote)

## 🔧 Setup and Installation

## Prerequisites

* Python 3.8+
* Google Colab account (for original development environment)
* Ollama installation for model serving
* Git and VS Code for repository management

## Key Dependencies

<pre class="not-prose w-full rounded font-mono text-sm font-extralight"><div class="codeWrapper text-textMainDark selection:text-super selection:bg-super/10 bg-offset dark:bg-offsetDark my-md relative flex flex-col rounded font-mono text-sm font-thin"><div class="translate-y-xs -translate-x-xs bottom-xl mb-xl sticky top-0 flex h-0 items-start justify-end"><button data-testid="copy-code-button" type="button" class="focus-visible:bg-offsetPlus dark:focus-visible:bg-offsetPlusDark hover:bg-offsetPlus text-textOff dark:text-textOffDark hover:text-textMain dark:hover:bg-offsetPlusDark dark:hover:text-textMainDark font-sans focus:outline-none outline-none outline-transparent transition duration-300 ease-out font-sans  select-none items-center relative group/button  justify-center text-center items-center rounded-full cursor-pointer active:scale-[0.97] active:duration-150 active:ease-outExpo origin-center whitespace-nowrap inline-flex text-sm h-8 aspect-square"><div class="flex items-center min-w-0 font-medium gap-1.5 justify-center"><div class="flex shrink-0 items-center justify-center size-4"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7999999999999998" stroke-linecap="round" stroke-linejoin="round" class="tabler-icon tabler-icon-copy "><path d="M7 7m0 2.667a2.667 2.667 0 0 1 2.667 -2.667h8.666a2.667 2.667 0 0 1 2.667 2.667v8.666a2.667 2.667 0 0 1 -2.667 2.667h-8.666a2.667 2.667 0 0 1 -2.667 -2.667z"></path><path d="M4.012 16.737a2.005 2.005 0 0 1 -1.012 -1.737v-10c0 -1.1 .9 -2 2 -2h10c.75 0 1.158 .385 1.5 1"></path></svg></div></div></button></div><div class="-mt-xl"><div><div data-testid="code-language-indicator" class="text-text-200 bg-background-300 py-xs px-sm inline-block rounded-br rounded-tl-[3px] font-thin">python</div></div><div class="pr-lg"><span><code><span><span class="token token"># Core RAG components</span><span>
</span></span><span>chromadb
</span><span>docling
</span><span><span>sentence</span><span class="token token operator">-</span><span>transformers
</span></span><span>
</span><span><span></span><span class="token token"># Model fine-tuning</span><span>
</span></span><span>transformers
</span><span>torch
</span><span>peft
</span><span>bitsandbytes
</span><span>
</span><span><span></span><span class="token token"># Ollama integration</span><span>
</span></span><span><span>ollama</span><span class="token token operator">-</span><span>python
</span></span><span></span></code></span></div></div></div></pre>

## 📊 Performance Characteristics

## RAG System Benefits

* **Contextual Accuracy** : Retrieves relevant information from Harry Potter novels[1](https://github.com/rupeshtr78/chroma-db-rag)[2](https://realpython.com/chromadb-vector-database/)
* **Personality Consistency** : Maintains Chandler Bing's characteristic humor and sarcasm
* **Efficient Retrieval** : ChromaDB enables fast similarity search across large document collections[1](https://github.com/rupeshtr78/chroma-db-rag)[2](https://realpython.com/chromadb-vector-database/)

## Fine-tuning Advantages

* **Specialized Knowledge** : Model trained specifically on Harry Potter content with Chandler's personality
* **Efficient Training** : QLoRA technique reduces memory requirements while maintaining performance[3](https://www.koyeb.com/tutorials/fine-tune-llama-3-1-8b-using-qlora-koyeb-serverless-gpus)[4](https://aws.amazon.com/blogs/machine-learning/fine-tune-meta-llama-3-1-models-for-generative-ai-inference-using-amazon-sagemaker-jumpstart/)
* **Scalable Deployment** : Ollama hosting enables easy model serving and integration

## 🎪 Unique Features

## Personality-Driven Responses

The system combines factual Harry Potter knowledge with Chandler Bing's distinctive characteristics:

* **Sarcastic Humor** : Responses include Chandler's trademark sarcasm
* **Pop Culture References** : Incorporates 90s references and Chandler's speaking patterns
* **Contextual Wit** : Maintains humor while providing accurate information

## Multi-Stage Architecture

* **Retrieval Layer** : ChromaDB for efficient document search[1](https://github.com/rupeshtr78/chroma-db-rag)[2](https://realpython.com/chromadb-vector-database/)
* **Generation Layer** : Fine-tuned Llama 3.1 model for personality-consistent responses[3](https://www.koyeb.com/tutorials/fine-tune-llama-3-1-8b-using-qlora-koyeb-serverless-gpus)[4](https://aws.amazon.com/blogs/machine-learning/fine-tune-meta-llama-3-1-models-for-generative-ai-inference-using-amazon-sagemaker-jumpstart/)[5](https://huggingface.co/blog/mlabonne/sft-llama3)
* **Integration Layer** : Seamless combination of retrieval and generation components

## 🔄 Future Enhancements

## Potential Improvements

* **Extended Content** : Include all 7 Harry Potter books for comprehensive coverage
* **Multi-Character Support** : Fine-tune models for other Friends characters
* **Interactive Interface** : Develop web-based chat interface for better user experience
* **Performance Optimization** : Implement caching mechanisms for faster response times[10](https://huggingface.co/learn/cookbook/en/semantic_cache_chroma_vector_database)

## Technical Upgrades

* **Model Quantization** : Optimize model size for deployment efficiency
* **Batch Processing** : Enable multiple query handling for scalability
* **Advanced Retrieval** : Implement hybrid search combining dense and sparse retrieval methods

## 📝 Development Notes

## Colab Limitations

* **State Management** : Encountered session state errors preventing direct GitHub integration
* **File Size Constraints** : Large model files required alternative hosting solutions
* **Resource Management** : GPU allocation limitations affected training duration

## Solutions Implemented

* **Local File Management** : Downloaded notebooks for local processing[6](https://graphite.dev/guides/how-to-push-code-from-vscode-to-github)
* **External Model Hosting** : Used Ollama for model deployment
* **Version Control Workflow** : Established VS Code-based Git workflow[6](https://graphite.dev/guides/how-to-push-code-from-vscode-to-github)[9](https://stackoverflow.com/questions/46175462/vs-code-git-push-is-not-pushing-the-code-to-remote)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues, feature requests, or pull requests to enhance the system's capabilities.

## 📜 License

This project is open-source and available under the MIT License.

*Could this BE any more of a unique RAG system?* 😄
