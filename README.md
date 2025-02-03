# MnemosyneRAG
A Lightweight RAG Implementation with ChromaDB and Caching.

## Getting Started

### Prerequisites

- Python 3.11
- Virtual Environment
- You will need to create a chroma_db vector db with two collections, kb_knowledge to store the KB data and query_cache to use it as temporal caching.

### Setting Up the Virtual Environment

1. **Create a Virtual Environment**:
   ```bash
   python3.11 -m venv venv
   ```

2. **Activate the Virtual Environment**:
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On macOS and Linux:
     ```bash
     source venv/bin/activate
     ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

## The Caching Magic

- Implemented a two-level caching system:
  - Quick in-memory LRU cache for embeddings
  - ChromaDB for storing responses persistently
- Made it thread-safe (because we like our data intact!)
- Easy to configure cache sizes based on your needs

## Performance

- Cache hits respond in under 50ms
- Background caching doesn't block responses
- Smart embedding reuse saves compute time
- Thread Pool keeps things smooth

## Smart Querying

- Semantic search that works
- Adjustable similarity settings
- Efficient vector handling
- Auto context enhancement

## Built With

- FastAPI
- ChromaDB
- OpenAI
- ThreadPoolExecutor
- Pydantic

## Environmental Variables

You must create an `.env` file with the following content:

```
OPENAI_API_KEY=<your_openai_api_key>
CLIENT_ID=some_key_for_client_id
CLIENT_SECRET=some_key_for_client_secret
ANONYMIZED_TELEMETRY=False # Disable telemetry on ChromaDB.
```

## Test

Open the Jupyter Notebook via VS Code and go step by step.
