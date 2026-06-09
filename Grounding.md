## Grounding in Agentforce

### RAG (Retrieval Augmented Generation) is a technique where an AI first retrieves relevant information from knowledge sources and then uses that information to generate a response.

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


### Search Types in RAG

#### Keyword Search

Finds results based on exact keyword matches.

**Example**

* Document: "Customer can reset password through the self-service portal."
* Query: "reset password" ✅
* Query: "change login credentials" ❌

**Best For:** IDs, product names, exact terms, codes.

---

#### Vector Search (Semantic Search)

Finds results based on meaning and intent rather than exact words.

**Example**

* Document: "Customer can reset password through the self-service portal."
* Query: "change login credentials" ✅
* Query: "recover account access" ✅

**Best For:** Natural language questions, knowledge articles, FAQs.

---

#### Hybrid Search

Combines Keyword Search and Vector Search.

**Example**

* Document: "Customer can reset password through the self-service portal."
* Query: "portal password change" ✅

Uses:

* Keyword Match: "portal"
* Semantic Match: "password change" ≈ "reset password"

**Best For:** Most Agentforce and RAG use cases.

---

### Key Takeaways

| Search Type    | Matches               | Best For                   |
| -------------- | --------------------- | -------------------------- |
| Keyword Search | Exact words           | IDs, codes, specific terms |
| Vector Search  | Meaning and intent    | Natural language queries   |
| Hybrid Search  | Exact words + meaning | Most RAG implementations   |

**Recommendation:** Hybrid Search is generally preferred because it combines the precision of keyword search with the intelligence of semantic search.


## Retrieval Augmented Generation (RAG)

### What is RAG?

RAG is a grounding technique that enhances LLM responses by retrieving relevant information from external knowledge sources and adding it to the prompt before generating a response.

### RAG Workflow

1. Retrieve relevant information from a knowledge source.
2. Augment the original prompt with the retrieved content.
3. Generate a response using the enriched prompt.

**Flow:** User Query → Retrieve → Augment → Generate

### Benefits

* Improves response accuracy and relevance.
* Reduces hallucinations.
* Uses up-to-date business knowledge.
* Supports both structured and unstructured data.

### Agentforce Data Library

A Data Library is a collection of content used by agents for retrieval.

Supported Sources:

* Salesforce Knowledge Articles
* Uploaded Files (PDF, Text, HTML)
* Web Search

### Answer Questions with Knowledge

Standard Agentforce action that:

* Searches the Data Library
* Retrieves relevant content
* Grounds the prompt
* Returns an accurate response

### Core RAG Components

#### Retriever

Fetches relevant information from the knowledge source.

#### Search Index

Stores searchable and optimized content.

#### Chunking

Breaks large documents into smaller sections for retrieval.

#### Vectorization

Converts text into numerical vectors for semantic search.

### Search Types

#### Keyword Search

* Matches exact words.
* Best for IDs, product names, and specific terms.

#### Vector Search

* Matches meaning and intent.
* Best for natural language queries.

#### Hybrid Search

* Combines keyword and vector search.
* Provides more accurate retrieval results.

### Data Preparation Process

1. Ingest Data
2. Chunk Content
3. Vectorize Content
4. Create/Search Index
5. Retrieve Relevant Information

### Key Takeaways

* RAG = Retrieve + Augment + Generate.
* Data Libraries provide business knowledge for agents.
* Retrievers fetch relevant content from search indexes.
* Chunking and vectorization enable semantic search.
* Hybrid Search combines exact matching and semantic matching.
* RAG helps Agentforce deliver accurate, context-aware, and up-to-date responses.


### Search Index

A Search Index is an optimized repository that stores chunked and vectorized content, enabling fast and accurate retrieval for RAG applications.

### Without a Search Index

When a user asks:

> "How do I reset my password?"

The system would need to scan every document, PDF, email, or knowledge article individually to find the answer.

**Problems:**

* Slow performance
* Higher processing cost
* Poor scalability
* Less accurate retrieval

### With a Search Index

Before runtime:

1. Ingest content
2. Chunk documents into smaller sections
3. Vectorize the chunks
4. Store them in a Search Index

At runtime:

User Query → Search Index → Retriever → Relevant Content → LLM Response

**Benefits:**

* Fast retrieval
* Better relevance
* Supports semantic search
* Scales to large knowledge repositories

### Example

Knowledge Base contains:

* Password Reset Guide
* Account Management Guide
* Billing FAQ
* Product Documentation

**User Query:**

> "I forgot my password and can't log in."

Without Search Index:

* System scans all documents manually.

With Search Index:

* Retriever instantly finds the Password Reset Guide and sends the relevant content to the LLM.

### What a Search Index Stores

* Content Chunks
* Metadata
* Keywords
* Vector Embeddings

### Key Takeaways

* Search Index is the foundation of RAG retrieval.
* Stores chunked and vectorized content.
* Enables fast and relevant information retrieval.
* Used by Retrievers to ground LLM responses.
* Supports Vector Search and Hybrid Search.
