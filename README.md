
# NLP Insurance Agent

A natural language processing system designed to answer questions about Turkish vehicle insurance (Kasko) policies using AI agents and retrieval-augmented generation (RAG).

## Overview

This project implements an intelligent insurance assistant that can understand and respond to questions about vehicle insurance policies in Turkish. The system uses advanced NLP techniques to extract information from insurance policy documents and provide accurate, contextual answers.

##  Features

-   **Document Processing**: Extracts and processes information from Anadolu Sigorta's insurance policy PDF
-   **RAG Architecture**: Implements Retrieval-Augmented Generation for accurate information retrieval
-   **AI Agent System**: Uses intelligent agents to handle complex queries
-   **Benchmark Testing**: Includes comprehensive performance evaluation
-   **Turkish Language Support**: Fully optimized for Turkish insurance terminology

##  Project Structure

```
NLP_insurance_agent/
├── ai_agent.ipynb              # Main notebook with AI agent implementation
├── kasko_kitapcigi_01_2024.pdf # Turkish vehicle insurance policy document
├── project report.pdf          # Detailed project documentation
├── benchmark_results.json      # Performance metrics and test results
├── requirements.txt            # Python dependencies
└── README.md                   # This file

```

##  Getting Started

### Prerequisites

-   Python 3.8+
-   Jupyter Notebook
-   Groq API Key
-   GPU recommended for optimal performance (optional)

### Installation

1.  Clone the repository:

```bash
git clone https://github.com/yyg27/NLP_insurance_agent.git
cd NLP_insurance_agent

```

2.  Install dependencies:

```bash
pip install -r requirements.txt

```

3.  Launch Jupyter Notebook:

```bash
jupyter notebook ai_agent.ipynb

```

## Usage

1.  Open `ai_agent.ipynb` in Jupyter Notebook
2.  Configure your Groq API key (or OpenAI API key) in the user created .env file or directly on notebook
3.  Run the cells sequentially to initialize the agent
4.  Input your insurance-related questions in Turkish
5.  The system will retrieve relevant information and generate accurate responses

### Example Queries

-   "Kasko sigortası nedir?"
-   "Trafik sigortası ile kasko arasındaki fark nedir?"
-   "Mini onarım teminatı neleri kapsar?"
-   "Cam hasarı teminatı nasıl çalışır?"
-   "Ferdi kaza sigortası primleri nasıl hesaplanır?"

## Performance & Benchmarking

The system's performance metrics are stored in `benchmark_results.json`. The agent has been evaluated on multiple dimensions using 50 diverse insurance-related questions.

### Evaluation Metrics

-   **Correctness**: Accuracy of information retrieved from policy documents
-   **Completeness**: Coverage of all aspects of the question
-   **Retrieval Quality**: How well retrieved chunks match the query
-   **Response Time**: Average latency to generate answers
-   **Hallucination Rate**: Frequency of fabricated information

### Benchmark Results (Groq Llama-3.3-70B)

```
Total Questions: 50

OVERALL METRICS:
   Correctness:        70.0%
   Completeness:       65.3%
   Retrieval Quality:  58.4%
   Avg Response Time:  29.93s
   Hallucination Rate: 0.0%

PERFORMANCE BY DIFFICULTY:
  Easy   (15 questions):  70.0%
  Medium (20 questions):  70.0%
  Hard   (15 questions):  70.0%

```

### Query Categories Tested

-   Policy coverage questions (Teminat sorguları)
-   Premium calculations (Prim hesaplamaları)
-   Claims procedures (Hasar süreçleri)
-   Coverage limitations and exclusions (İstisnalar)
-   Comparison queries (Farklılık sorguları)

The system demonstrates **consistent 70% accuracy** across all difficulty levels with **zero hallucination**, ensuring reliable information delivery. Full benchmark details available in `benchmark_results.json`.

##  Technical Stack

-   **NLP Framework**: LangChain for agent orchestration
-   **LLM Backend**: Groq Llama-3.3-70B (primary), OpenAI GPT models (alternative)
-   **Vector Database**: FAISS / ChromaDB for semantic search
-   **Document Processing**: PyPDF2, pdfplumber for PDF extraction
-   **Embeddings**: OpenAI Ada-002 / Sentence Transformers
-   **Text Splitting**: RecursiveCharacterTextSplitter

### Known Limitations

**Google Gemini API Compatibility Issue**: This project currently does not support Google Gemini models due to API integration challenges and rate limiting constraints encountered during development. So benchmark comparison between Groq Llama-3.3-70B and Google Gemini is not completed

##  Documentation

For detailed information about the system architecture, methodology, and results, please refer to `project report.pdf`.


## Authors
- Yusuf Yiğit Gültekin 2023556458




----------


