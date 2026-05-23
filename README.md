# AI-Powered Personal Knowledge Base

This project implements a fully localized Personal Knowledge Management (PKM) system built with Obsidian and Ollama. It leverages Retrieval-Augmented Generation (RAG) to allow an AI assistant to query, summarize, and reflect upon a locally stored Markdown vault.

## Project Structure
The repository is structured around an Obsidian vault that contains a minimum of 25 markdown notes categorized across specific domains:
- `01-Learning/`: Technical concepts and study notes (e.g., DSA, time complexity).
- `02-Career-Interview/`: Interview preparation and behavioral stories (STAR method).
- `03-Projects/`: Project tracking and architectural decisions.
- `04-Content/`: Summaries of books, videos, and articles.
- `05-Ideas/`: Fleeting thoughts and brainstorming.
- `06-Mistakes/`: Detailed logs of coding errors, following a strict Goal/Problem/Fix structure.

The vault root includes a `Dashboard.md` file powered by the Dataview plugin to provide dynamic queries of the knowledge base.

## Prerequisites
- **Obsidian**: A local-first Markdown note editor.
- **Docker & Docker Compose**: To run the local Ollama LLM service.
- **Obsidian Plugins**:
  - `Dataview`: For querying notes.
  - `Smart Connections`: For connecting to the local Ollama instance and enabling AI chat.

## Setup Instructions
1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd obsidian-ollama-rag
   ```

2. **Start the Local AI Service**:
   Use Docker Compose to launch Ollama and pull the `llama3.2` model automatically.
   ```bash
   docker-compose up -d
   ```
   *Note: Ensure you have at least 8GB of RAM available. Wait a moment for the model to pull.*

3. **Open the Obsidian Vault**:
   - Open Obsidian and select "Open folder as vault".
   - Select the root directory of this repository.

4. **Enable Plugins**:
   - Go to Settings > Community Plugins and ensure Safe Mode is off.
   - Enable `Dataview` and `Smart Connections`.
   - The Smart Connections plugin is pre-configured to connect to `localhost:11434` using the `llama3.2` model.

5. **Trigger Vault Indexing**:
   - Open the Command Palette in Obsidian (`Ctrl+P` or `Cmd+P`), type `Smart Connections: Force re-index`, and execute it to generate vector embeddings for the notes.

## Observations
Building this local RAG pipeline demonstrates the incredible utility of owning your data and processing it locally. 
- The `06-Mistakes` folder structure proved extremely helpful for the AI to identify patterns in errors.
- The Smart Connections plugin seamlessly handles the embedding and retrieval process without sending any data to external servers, providing an enterprise-grade AI experience directly on a personal machine.

## Deliverables
Check the `deliverables/` folder for the simulated AI interaction logs (`ai_interaction_log.md`) and a detailed reflection on the system (`ai_reflection.md`).
