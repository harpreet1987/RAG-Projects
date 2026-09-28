> 📌 **Note:** This repository is a fork of the original project by [kiran-001](https://github.com/kiran-001/RAG-Projects.git), used for learning and reference purposes. All credit for these projects goes to the original author. I'm using this to practice and build my own AI projects.

---


This repository showcases a collection of advanced chatbot projects that demonstrate **Question-Answering (Q&A)** and **Retrieval-Augmented Generation (RAG)** techniques with Large Language Models across various types of data sources. Each project focuses on integrating LLMs with different databases and tools (including vector databases, graph databases, SQL databases, and tabular data) to create intelligent Q&A systems. The projects serve as a proof of expertise in designing complex LLM-driven applications and are implemented using both OpenAI and Azure OpenAI services.

## Projects

* **LangGraph_1o1_Agentic_Customer_Support:** An agentic customer service chatbot for an airline, built using a graph-of-tools approach. It demonstrates how to integrate *multiple tools* (knowledge retrieval, web search, planning, etc.) within an LLM agent to handle complex user requests in a customer support domain.

* **AgentGraph-Intelligent-Q&A-and-RAG-System:** An intelligent Q&A system that combines *SQL database agents* with *RAG* for unstructured data. This project shows how an LLM agent can automatically choose between querying structured databases and performing document retrieval to answer questions, scaling to large multi-database environments.

* **Q&A-and-RAG-with-SQL-and-TabularData:** A chatbot interface that lets users query *relational databases and spreadsheets (CSV/XLSX)* in natural language. It uses GPT-3.5 with LangChain to run SQL queries on a sample database and perform RAG on tabular data (via a vector store of embeddings), enabling conversational analytics on structured data.

* **KnowledgeGraph-Q&A-and-RAG-with-TabularData:** A Q&A system that leverages a *knowledge graph* constructed from tabular data. Using Neo4j and an LLM-based graph agent, it allows natural language questions to be answered by traversing a knowledge graph (for structured relationships) and by RAG on content derived from the same data, illustrating how structured and unstructured data can be combined.

## Project Structure

Each project in the repository follows a similar structure for consistency:

```
ProjectName/
├── README.md          <- Top-level documentation for the project.
├── HELPER.md          <- Additional notes or tips for running the project.
├── .env               <- Environment variable definitions (API keys, config options).
├── .here              <- Marker file for project root (used by some tools).
├── configs/           <- YAML configuration files for various settings and tools.
├── explore/           <- Jupyter notebooks for exploration and prototyping.
├── data/              <- Sample datasets and databases for the project.
├── src/               <- Source code for the project implementation.
│   └── utils/         <- Utility modules and helper functions.
└── images/            <- Images used in the README or app UI.
```

*Note:* The exact contents may vary slightly by project (depending on specific needs), but this general layout is maintained across all four projects.

## Key Considerations

* **Use of OpenAI Models:** All projects are built on OpenAI's GPT models (e.g. GPT-3.5), accessed via OpenAI or Azure OpenAI APIs. Ensure you have the appropriate API keys and access for running the applications.

* **Database Safety:** If connecting an agent to a database, use read-only access or a restricted dataset for safety. These projects illustrate interactions with databases; in practice, never give an LLM agent unrestricted write/delete permissions on production data.

* **Schema and Naming:** Well-structured schemas and clear, descriptive column names in your databases/tables will help the LLM agents navigate and understand the data more effectively.

* **User Expertise:** Familiarity with database query languages (SQL for relational data, Cypher for graph data, or Pandas for CSV) is beneficial. While the chatbots handle query generation, knowing how data is structured will help users ask better questions and interpret responses.
