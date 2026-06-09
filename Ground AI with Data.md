## Why Ground AI with Data?

AI models are trained on general-purpose data and lack organization-specific knowledge. Grounding provides trusted business data to the LLM, enabling more accurate, relevant, and context-aware responses.

### Benefits of Grounding

* Improves response accuracy.
* Reduces hallucinations.
* Uses current business information.
* Delivers context-specific recommendations and answers.

### Enterprise Data Challenge

Most enterprise knowledge exists in unstructured formats such as:

* PDFs
* Emails
* Documents
* Chat Logs
* Images
* Videos
* Social Media Content

This data contains valuable business insights but is difficult to search efficiently.

### Agentforce Data Library

Agentforce Data Library connects enterprise data to Salesforce AI features and automatically creates:

* Data Streams
* Search Indexes
* Retrievers
* Prompt Resources

This enables agents to access relevant business knowledge during runtime.

### Core Concepts

#### Grounding

Adding domain-specific knowledge to prompts before sending them to the LLM.

#### Chunking

Breaking large documents into smaller meaningful sections for efficient retrieval.

**Example:**
100-page PDF → Paragraphs/Sections → Chunks

#### Search Index

An optimized repository that stores chunked and searchable content for fast retrieval.

#### Retriever

A component that searches the index and retrieves relevant information for a user query.

### Setup Process

1. Ingest Data
2. Create Data Stream
3. Map Data Objects
4. Chunk Content
5. Build Search Index
6. Create Retriever

### Runtime Flow

User Query
→ Prompt Template
→ Retriever
→ Search Index
→ Retrieve Relevant Content
→ Augment Prompt
→ LLM Response

### Key Takeaways

* Grounding helps AI use trusted business knowledge.
* Chunking improves retrieval efficiency.
* Search Index enables fast and relevant searches.
* Retrievers fetch the most relevant content.
* Agentforce Data Library automates the setup of RAG components.
* Grounded AI provides more accurate and context-aware responses.
