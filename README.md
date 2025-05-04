# SQL_ChatBot_LlamaIndex

A natural language interface for querying SQL databases using LlamaIndex and LLMs.

## Overview

This project provides a conversational interface to query SQL databases using natural language. It leverages:
- LlamaIndex for query processing
- Large Language Models for text-to-SQL conversion
- Query validation and correction capabilities

## Features

- Convert natural language questions to SQL queries
- Query validation to ensure accurate responses
- Automatic retry mechanism for failed queries
- Support for multiple tables and complex queries
- Handles SQL database schema understanding

## Setup

### Prerequisites

- Python 3.x
- Access to a SQL database
- OpenAI API key

### Installation

1. Clone this repository
2. Install dependencies:
```
pip install -r requirements.txt
```
3. Set up your OpenAI API key as an environment variable:
```
export OPENAI_API_KEY=your_api_key_here
```

## Usage

The project includes a Jupyter notebook (`llama_index/v1.ipynb`) that demonstrates the workflow:

1. Connect to your SQL database
2. Define the database schema
3. Configure the query engine
4. Create an agent to handle natural language queries
5. Query your database with natural language questions

## Dependencies

- llama-index - Core framework for the chatbot
- langchain, langchain_openai - LLM integration
- sqlalchemy - SQL database connectivity
- openai - OpenAI API integration
- fastapi, uvicorn - For API deployment (optional)
- pandas, numpy - Data processing
- plotly, matplotlib, kaleido - For visualization (optional)

## Example

```python
# Connect to database
sql_database = SQLDatabase(engine=engine, schema="YourSchema")

# Create query engine
sql_query_engine = NLSQLTableQueryEngine(
    sql_database=sql_database,
    tables=["YourTables"],
    verbose=True
)

# Run queries
response = agent.chat("What is the total sales for January 2023?")
```

