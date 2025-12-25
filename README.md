# LangChain Integration Examples

A collection of practical examples demonstrating how to integrate various Large Language Models (LLMs) and embedding models using LangChain framework.

## Overview

This repository contains working examples of LangChain integrations with multiple AI providers, including OpenAI, Anthropic, Google Gemini, and HuggingFace. These examples serve as quick-start templates for building LLM-powered applications.

## Features

- **Multiple LLM Providers**: Examples for OpenAI, Anthropic Claude, Google Gemini, and HuggingFace models
- **Embedding Models**: Implementations using OpenAI and HuggingFace embeddings
- **Local & API Options**: Support for both local model execution and API-based approaches
- **Production-Ready**: Clean, modular code structure with environment variable management

## Examples Included

### Chat Models

1. **OpenAI ChatGPT** (`1_chatmodel_openai.py`)
   - Model: GPT-4
   - Custom temperature and token limits
   - Creative text generation example

2. **Anthropic Claude** (`2_chatmodel_anthropic.py`)
   - Model: Claude Opus 4.1
   - Latest generation Claude model
   - Simple Q&A implementation

3. **Google Gemini** (`3_chatmodel_google.py`)
   - Model: Gemini 2.5 Flash
   - Fast inference with Google's latest model
   - Straightforward integration

4. **HuggingFace API** (`4_chatmodel_hf_api.py`)
   - Remote inference via HuggingFace endpoints
   - Model: TinyLlama-1.1B-Chat
   - API-based approach

5. **HuggingFace Local** (`5_chatmodel_hf_local.py`)
   - Local model execution
   - Custom cache directory configuration
   - Pipeline-based inference

### Embedding Models

1. **OpenAI Embeddings - Query** (`1_embedding_openai_query.py`)
   - Single text embedding generation
   - Model: text-embedding-3-large
   - Custom dimensions (132)

2. **OpenAI Embeddings - Documents** (`2_embedding_openai_docs.py`)
   - Batch document embedding
   - Multiple text vectorization
   - Same model configuration

3. **HuggingFace Embeddings - Local** (`3_embedding_hf_local.py`)
   - Local embedding generation
   - Model: sentence-transformers/all-MiniLM-L6-v2
   - No API calls required

## Prerequisites

- Python 3.8+
- pip package manager
- API keys for respective services (OpenAI, Anthropic, Google, HuggingFace)

## Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd <repository-name>
```

2. Install required dependencies:
```bash
pip install langchain-openai langchain-anthropic langchain-google-genai langchain-huggingface python-dotenv
```

3. Create a `.env` file in the root directory:
```env
OPENAI_API_KEY=your_openai_api_key_here
ANTHROPIC_API_KEY=your_anthropic_api_key_here
GOOGLE_API_KEY=your_google_api_key_here
HUGGINGFACEHUB_API_TOKEN=your_huggingface_token_here
```

## Usage

Run any example script:

```bash
# Chat model examples
python 1_chatmodel_openai.py
python 2_chatmodel_anthropic.py
python 3_chatmodel_google.py
python 4_chatmodel_hf_api.py
python 5_chatmodel_hf_local.py

# Embedding examples
python 1_embedding_openai_query.py
python 2_embedding_openai_docs.py
python 3_embedding_hf_local.py
```

## Configuration Notes

### HuggingFace Local Model
- The local HuggingFace example uses a custom cache directory
- Modify `HF_HOME` in the script to match your system path:
```python
os.environ['HF_HOME'] = '/path/to/your/huggingface_cache'
```

### Model Parameters
Each example can be customized with different parameters:
- `temperature`: Controls randomness (0.0 - 2.0)
- `max_tokens` / `max_new_tokens`: Limits response length
- `dimensions`: Embedding vector size (for OpenAI embeddings)

## API Keys Setup

### OpenAI
Get your API key from: https://platform.openai.com/api-keys

### Anthropic
Sign up for access at: https://console.anthropic.com/

### Google AI
Create API key at: https://makersuite.google.com/app/apikey

### HuggingFace
Generate token at: https://huggingface.co/settings/tokens

## Project Structure

```
.
├── 1_chatmodel_openai.py          # OpenAI GPT-4 chat example
├── 2_chatmodel_anthropic.py       # Anthropic Claude chat example
├── 3_chatmodel_google.py          # Google Gemini chat example
├── 4_chatmodel_hf_api.py          # HuggingFace API chat example
├── 5_chatmodel_hf_local.py        # HuggingFace local chat example
├── 1_embedding_openai_query.py    # OpenAI query embedding
├── 2_embedding_openai_docs.py     # OpenAI document embeddings
├── 3_embedding_hf_local.py        # HuggingFace local embeddings
├── .env                            # Environment variables (create this)
└── README.md                       # This file
```

## Use Cases

These examples can be used as building blocks for:
- **RAG Systems**: Document embeddings for semantic search
- **Chatbots**: Multi-provider chat interfaces
- **Content Generation**: Creative writing and text generation
- **Semantic Search**: Vector similarity matching
- **AI Agents**: Foundation for agentic AI applications

## Technologies Used

- [LangChain](https://www.langchain.com/) - LLM application framework
- [OpenAI](https://openai.com/) - GPT models
- [Anthropic](https://www.anthropic.com/) - Claude models
- [Google AI](https://ai.google.dev/) - Gemini models
- [HuggingFace](https://huggingface.co/) - Open-source models

## Contributing

Feel free to submit issues or pull requests for improvements or additional examples.

## License

MIT License - feel free to use these examples in your projects.



---

**Note**: Remember to never commit your `.env` file or expose API keys in your code. Add `.env` to your `.gitignore` file.
