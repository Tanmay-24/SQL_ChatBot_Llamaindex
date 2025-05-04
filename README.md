# PDF-Demo-Chatbot

A system for extracting, processing, and querying construction project PDF documents using vector search.

## Overview

This project provides tools to:
- Extract content from PDF documents containing construction project specifications and submittals
- Process and transform the extracted data
- Store document embeddings in Milvus vector database
- Query the documents through a vector search API

## Setup

### Prerequisites

- Python 3.x
- Docker and Docker Compose

### Installation

1. Clone this repository
2. Install dependencies:
```
pip install -r requirements.txt
```
3. Start Milvus and related services:
```
docker-compose up -d
```

## Usage

The project includes several Jupyter notebooks that demonstrate different parts of the workflow:

- `pdf_extract.ipynb` - Extract text from PDF documents
- `pdfcontent_extract_footer_based.ipynb` - Extract content with footer-based processing
- `Vectordb.ipynb` - Work with the vector database
- `service_test.ipynb` - Test the service endpoints

## Dependencies

- fastapi - Web API framework
- uvicorn - ASGI server
- milvus - Vector database
- transformers - For embedding generation
- pandas, numpy - Data processing
- torch - Machine learning backend
- towhee - Data processing pipeline

## Architecture

The system uses a Docker-based deployment with:
- Milvus standalone server
- MinIO for object storage
- etcd for metadata storage

