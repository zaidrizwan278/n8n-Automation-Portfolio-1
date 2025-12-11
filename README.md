# **n8n AI Automation Portfolio** 1 🤖



A collection of advanced **n8n workflows** automating business processes using AI Agents, RAG (Retrieval-Augmented Generation), and integrations with Gmail, Google Sheets, and Pinecone.



### 📂 Projects



##### 1\. RAG Knowledge Base (Chat with Data)

A system to upload documents and "chat" with them using OpenAI and Pinecone.

\* **rag-ingestion.json**: Downloads files from OneDrive, creates embeddings, and upserts to Pinecone.
* **Function:** The "learning" pipeline for the AI.
* **Features:** Downloads documents from **OneDrive**, splits the text, and stores embeddings in **Pinecone** to create a searchable knowledge base.

\* **rag-chat.json**: An AI Agent that searches the Pinecone index to answer user queries.
    * **Function:** The "retrieval" interface.
    * **Features:** A chatbot that answers questions based *only* on the private data stored in the Pinecone Vector Store (setup in the workflow above).



##### 2\. Inventory Management Agent

\* **inventory-agent.json**

\* Function: An AI employee that manages stock levels via chat. It can search for items or update quantities in Google Sheets.

\* Features: Checks stock levels and updates item quantities in Google Sheets via natural language.

\* Tech Stack: OpenAI, Google Sheets, LangChain.

\* Setup: Requires a Google Sheet with columns: Item names and Quantity.



##### 3\. Smart Email Manager (Inbox Zero)

\* **email-classifier.json**

\* Function: Reads incoming emails and uses an LLM to categorize them (Sponsorship, High Priority, Test). It auto-drafts responses for important mails.
\* Features:
    * **Classifies** emails into categories (e.g., Sponsorship, High Priority, Test).
    * **Drafts Replies:** Automatically writes context-aware replies for high-priority emails using GPT-4.
    * **Drafts:** Saves the response as a draft in Gmail for review.



##### 4\. Simple Mail Sender

\* gmail-sender.json

\* Function: A tool to send emails quickly using natural language commands like "Send a report to Bob."
* **Features:** Takes a user prompt (e.g., "Send an email to Bob about the meeting") and executes the action using the Gmail tool.



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


