## Grounding in Agentforce

### RAG is a grounding technique where relevant information is retrieved from a knowledge source and added to the prompt before sending it to the LLM, resulting in more accurate and context-aware responses.

### What is Grounding?

Grounding is the process of providing an LLM with relevant business data before generating a response. This improves accuracy, relevance, and trustworthiness.

### Benefits

* Reduces hallucinations
* Uses current and reliable information
* Improves agent decision-making
* Generates more context-aware responses

### Types of Grounding Data

#### Structured Data

Organized data with predefined formats.
Examples:

* Salesforce Accounts
* Contacts
* Cases
* Data Model Objects (DMOs)
* Spreadsheets

#### Unstructured Data

Data without a predefined structure.
Examples:

* PDFs
* Emails
* Chat Logs
* Documents
* Social Media Posts

### Retrieval Augmented Generation (RAG)

RAG is a grounding technique that retrieves relevant information from unstructured data sources and adds it to the LLM prompt before generating a response.

**Flow:**
User Query → Retrieve Relevant Data → Enrich Prompt → Generate Response

### Key Takeaways

* Grounding provides trusted data to LLMs.
* Structured data is easier to search and analyze.
* Unstructured data often requires preprocessing.
* RAG enhances responses using relevant information from knowledge sources.
* Grounding improves accuracy, relevance, and reliability of Agentforce responses.

## Retrieval Augmented Generation (RAG)

### What is RAG?

Retrieval Augmented Generation (RAG) is a grounding technique that improves LLM responses by retrieving relevant business knowledge and adding it to the prompt before generating a response.

### How RAG Works

1. Retrieve relevant information from a knowledge source.
2. Augment the original prompt with the retrieved information.
3. Generate a response using the enriched prompt.

**Flow:**
User Query → Retrieve Knowledge → Augment Prompt → LLM Response

### Benefits

* Improves accuracy and relevance.
* Reduces hallucinations.
* Uses up-to-date business knowledge.
* Supports both structured and unstructured data sources.

### Agentforce Data Library

A Data Library is a collection of content used by agents to answer questions.

Supported sources:

* Salesforce Knowledge Articles
* Uploaded Files (PDF, HTML, Text)
* Web Search

### Answer Questions with Knowledge Action

Standard Agentforce action used to:

* Search the Data Library
* Retrieve relevant content
* Ground the prompt
* Return a more accurate response

### RAG Components

* **Retriever** – Finds relevant information.
* **Search Index** – Stores searchable content.
* **Chunking** – Breaks content into smaller pieces.
* **Vectorization** – Converts text into numerical vectors for semantic search.
* **Prompt Template** – Combines retrieved content with the user query.

### Search Types

* **Vector Search** – Finds content based on meaning (semantic similarity).
* **Hybrid Search** – Combines vector search and keyword search.

### Key Takeaways

* RAG = Retrieve + Augment + Generate.
* Data Libraries provide business knowledge for agents.
* Retrievers fetch relevant information from search indexes.
* Chunking and vectorization prepare data for semantic search.
* RAG helps Agentforce deliver more accurate and context-aware responses.
