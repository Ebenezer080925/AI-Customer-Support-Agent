# STONES: AI Customer Support Agent for Dao Confectiones

An intelligent, context-aware customer support workflow built with **n8n** to automate booking requests, handle menu inquiries via RAG (Retrieval-Augmented Generation), and manage human support handoffs for a catering business.

![n8n Workflow Architecture](https://github.com/Ebenezer080925/AI-Customer-Support-Agent/blob/main/Screenshot%202026-10-15%20151319.png)

## 🛠️ System Architecture & Tech Stack

This workflow operates entirely via webhook integrations and leverages a suite of AI and database tools:

*   **Orchestration:** n8n 
*   **LLM:** Groq (`qwen/qwen3.8-27b`) acting as the core conversational agent.
*   **Embeddings:** Google Gemini (`gemini-embedding-2`) for vectorizing knowledge base documents.
*   **Vector Store & Memory:** PostgreSQL (PGVector) for storing business policies, menu items, and maintaining long-term chat session memory.
*   **Integrations:** Gmail API for routing confirmed orders to the kitchen and escalating issues to human support.

## ✨ Core Features

*   **Automated Order Collection:** The AI systematically collects mandatory details (Name, Email, Delivery/Pickup, Cake Specs, Date/Time) before allowing an order to proceed.
*   **Knowledge Base Retrieval:** Uses PGVector to dynamically fetch exact pricing, ingredients, and store policies rather than hallucinating answers.
*   **Smart Handoff Protocol:** Automatically detects when a user is frustrated or requests a manager, collects their contact details, and routes a support ticket to staff via email.
*   **Stateful Conversations:** Maintains user session history via Postgres Chat Memory, allowing for natural, multi-turn conversations.

![](https://github.com/Ebenezer080925/AI-Customer-Support-Agent/blob/main/Screenshot%202026-10-15%20151944.png)
Order being sent to the kitchen and they reply under your mail when approved 
Canibe connected to an website to act as the human customer support Agent 

# ![Json](https://github.com/Ebenezer080925/AI-Customer-Support-Agent/blob/main/ED%20confectiones%20Booking%20flow%20Agent.json)
