# MnemosyneRAG
A Lightweight RAG Implementation with ChromaDB and Caching.

## The Caching Magic

* I implemented a two-level caching system:
* Quick in-memory LRU cache for embeddings
* ChromaDB for storing responses persistently
* Made it thread-safe (because we like our data intact!)
* Easy to configure cache sizes based on your needs

## Performance

* Cache hits respond in under 50ms
* Background caching doesn't block responses
* Smart embedding reuse saves compute time
* Thread Pool keeps things smooth

## Smart Querying

* Semantic search that works
* Adjustable similarity settings
* Efficient vector handling
* Auto context enhancement

## Built With

* FastAPI
* ChromaDB
* OpenAI
* ThreadPoolExecutor
* Pydantic
