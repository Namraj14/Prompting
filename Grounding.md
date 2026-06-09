## Grounding in Agentforce

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

