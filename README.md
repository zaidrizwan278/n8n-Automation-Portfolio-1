# **n8n AI Automation Portfolio** 1 🤖



A collection of advanced **n8n workflows** automating business processes using AI Agents, RAG (Retrieval-Augmented Generation), and integrations with Gmail, Google Sheets, and Pinecone.



### 📂 Projects



##### 1\. RAG Knowledge Base (Chat with Data)

A system to upload documents and "chat" with them using OpenAI and Pinecone.

\* **rag-ingestion.json**: Downloads files from OneDrive, creates embeddings, and upserts to Pinecone.

\* **rag-chat.json**: An AI Agent that searches the Pinecone index to answer user queries.



##### 2\. Inventory Management Agent

\* **inventory-agent.json**

\* Function: An AI employee that manages stock levels via chat. It can search for items or update quantities in Google Sheets.

\* Setup: Requires a Google Sheet with columns: Item names and Quantity.



##### 3\. Smart Email Manager (Inbox Zero)

\* **email-classifier.json**

\* Function: Reads incoming emails and uses an LLM to categorize them (Sponsorship, High Priority, Test). It auto-drafts responses for important mails.



##### 4\. Simple Mail Sender

\* gmail-sender.json

\* Function: A tool to send emails quickly using natural language commands like "Send a report to Bob."



---



##### 🛠️ Setup



1\. **Import**: In n8n, go to **Add Workflow** > **Import from File** and select the JSONs.

2\. **Credentials**: You must configure your own credentials for:

&nbsp;  \* OpenAI API

&nbsp;  \* Pinecone (for RAG)

&nbsp;  \* Google Cloud (Gmail/Sheets)

&nbsp;  \* Microsoft OneDrive (for RAG ingestion)



##### 📄 License

This project is licensed under the MIT License - see the \[LICENSE](LICENSE) file for details.

