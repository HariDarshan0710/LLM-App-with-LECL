### GitHub README: LLM App Using LangChain Expressions and FastAPI

---

# LLM Translation App: French to Kannada

This repository demonstrates the creation of a basic LLM-based app using **LangChain Expression Language (LCEL)**. It showcases building and deploying **LLM, Prompt, and Structured Output Chains** with LangChain, integrated into an API using **LangServe** and **FastAPI**. The app focuses on **translating text from French to Hindi**.

---

## Features
- **LangChain Expressions**: Constructs chains for LLM, prompts, and structured outputs.
- **LangServe Deployment**: Deploys the LLM chain as an API.
- **FastAPI Integration**: Provides a client-server architecture for the translation service.
- **French to Hindi Translation**: Utilizes the QROQ API for enhanced translation accuracy.

---

## Prerequisites
- Python 3.8+
- API keys for QROQ
- LangChain, FastAPI, and other required dependencies

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/llm-translation-app.git
   cd llm-translation-app
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up environment variables for QROQ API in `.env`:
   ```plaintext
   QROQ_API_KEY=<your-api-key>
   ```

---

## Usage

### Start the API Server
Run the FastAPI server using the following command:
```bash
uvicorn server:app --reload
```

### Make Translation Requests
Send a POST request to the API endpoint:
```http
POST http://localhost:8000/translate
Content-Type: application/json
{
  "text": "Bonjour"
}
```

Response:
```json
{
  "translation": "नमस्ते"
}
```

---

## File Structure
```
📁 llm-translation-app
├── server.py               # FastAPI server
├── client.py               # Client script for testing
├── chains/                 # LangChain expressions and chains
├── .env                    # Environment variables
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

---

## Deployment
Use **LangServe** to deploy the LLM chain as an API:
```bash
langserve deploy chains/translation_chain.yaml
```

---

## Future Improvements
- Add support for more languages.
- Optimize translation using fine-tuned LLMs.
- Enhance the API for scalability.

---
