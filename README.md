# RAGOMEGA AI: Generic Retrieval-Augmented Generation (RAG) Application

## Project Overview

RAGOMEGA AI is a dynamic chatbot application that leverages cutting-edge language models for both general-purpose queries and real-time information retrieval. In addition to answering general questions, users can upload their own documents (e.g., PDFs) and ask the chatbot specific questions based on the document content. This dual functionality combines the strengths of AI-driven responses and document-based insights.

## Core Technologies

- **Frontend**: Next.js
- **Authentication & Authorization**: NextAuth.js
- **AI/LLM Handling**: LangChain
- **Backend Integration**: FastAPI
- **Database**: MongoDB

## Key Features

### 1. Chatbot Functionality (LLM-Based Responses)
- **General Queries**: Users can ask any general-purpose question, and the chatbot will provide answers using the integrated Language Model (e.g., GPT).
- **Real-Time Information Retrieval**: For live queries such as weather updates or stock prices, the chatbot uses LangChain's browser API to fetch the latest data and return real-time information.

### 2. RAG (Retrieval-Augmented Generation) Feature
- **Document Upload**: Users can securely upload PDF documents that will be associated with their account.
- **Document-Specific Q&A**: Users can ask questions about the content of their uploaded documents, and the chatbot will retrieve relevant sections and generate precise answers based on the document's content.

## Project Structure

### 1. Frontend (Next.js)
The frontend is built with Next.js to create a responsive, fast, and user-friendly interface. Key pages include:
- **Home Page**: An introduction to the chatbot’s features and capabilities.
- **Chatbot Interface**: A chat interface for interacting with the LLM.
- **Document Upload**: A page where users can upload PDF documents for RAG-based Q&A.

### 2. Authentication & Authorization (NextAuth.js)
- **Authentication**: Users must create an account or log in to access key features (e.g., chatbot, document upload).
- **Social Login**: Supports logging in with Google, GitHub, and other providers.
- **Access Control**: Ensures secure access to private content and features.

### 3. AI Handling (LangChain)
- **LLM Integration**: LangChain manages the connection to language models for AI-based responses.
- **Real-Time Queries**: LangChain’s browser API handles data fetching for real-time information (e.g., “What's the weather in London?”).

### 4. Backend API (FastAPI)
- **FastAPI**: Acts as the backend server to process user requests, handle document uploads, and interact with the LLM.
- **File Management**: Provides endpoints for managing uploaded files (e.g., upload, retrieval, and deletion).
- **RAG Process**: Extracts relevant text from uploaded documents and sends it to the LLM for response generation.

### 5. Database (MongoDB)
- **User Data**: MongoDB stores user credentials, authentication details, and manages user-specific data.
- **Document Storage**: Uploaded documents are securely stored and linked to user accounts for customized interactions.

## User Flow

1. **Login/Sign-Up**: Users register or log in using email or social login via NextAuth.js. 
2. **Chat Interaction**: 
   - Users ask general queries, and the chatbot responds using the LLM.
   - For real-time queries, the chatbot retrieves live information through LangChain.
3. **Document-Specific Interaction**: 
   - Users upload PDFs, and the system securely stores them.
   - Users can then ask questions about the document, and the system will retrieve relevant sections and provide answers.

## Pages

### 1. Home Page
- Overview of the chatbot’s general AI capabilities and RAG-based Q&A.
- Call to action: buttons to start chatting or upload a document.

### 2. Login/Sign-Up Page
- Users can sign up or log in via email or social providers using NextAuth.js.
- Required to access core features (e.g., chatbot and document upload).

### 3. Chatbot Page (LLM Interaction)
- Chat interface for users to ask general or real-time queries.
- Clean, simple UI with chat history viewing.

### 4. Generic RAG Page (Document Upload & Q&A)
- Users upload PDFs for document-specific Q&A.
- The chatbot answers questions based on the content of the uploaded documents.

## Project Goals

The RAGOMEGA AI application aims to provide a flexible, user-friendly chatbot that:
1. **Delivers AI-based responses** to general-purpose queries using LLMs.
2. **Offers real-time information retrieval** for live queries.
3. **Supports document-specific Q&A** with RAG functionality, giving users the power to upload documents and receive insights directly from their own content.

## Getting Started

### Prerequisites
- **Node.js**: Ensure you have Node.js installed.
- **MongoDB**: Set up a MongoDB instance for user data and document storage.
- **FastAPI**: Make sure FastAPI is properly configured on your backend.
- **LangChain**: Use LangChain for AI model integration and real-time queries.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/username/ragomega-ai.git
   cd ragomega-ai
