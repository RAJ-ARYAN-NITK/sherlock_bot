I'll update the README to remove the folder structure and add links for the API and the live app.

```markdown:c:\Users\admin\OneDrive\Desktop\sherlock_bot\README.md
# 🕵️ Sherlock Holmes Detective Chatbot

A sophisticated AI-powered chatbot that embodies the character of Sherlock Holmes, the world's greatest consulting detective. This application allows users to interact with a virtual Sherlock Holmes who responds to queries with the deductive reasoning and Victorian-era flair characteristic of Sir Arthur Conan Doyle's iconic character.

## 📋 Overview

The Sherlock Holmes Detective Chatbot combines modern AI technology with classic literature to create an immersive conversational experience. The system uses Retrieval-Augmented Generation (RAG), natural language processing, and vector embeddings to provide contextually relevant and character-authentic responses.

## 🔍 Features

- **Character-Authentic Responses**: Interact with an AI that responds in the distinctive style and manner of Sherlock Holmes
- **Knowledge Base**: Built on the complete works of Sherlock Holmes by Sir Arthur Conan Doyle
- **Victorian-Era UI**: A thematically appropriate user interface that evokes the aesthetic of 221B Baker Street
- **Word-by-Word Response Animation**: Responses appear gradually, simulating the detective's thoughtful deduction process
- **Conversation Management**: Start new investigations or continue existing ones with conversation tracking

## 🛠️ Technology Stack

### Backend
- **FastAPI**: High-performance Python web framework for building the API
- **Mistral AI**: Advanced language model for generating contextually relevant responses
- **ChromaDB**: Vector database for storing and retrieving text embeddings
- **Sentence Transformers**: For creating semantic embeddings of text
- **RAG (Retrieval-Augmented Generation)**: Enhances LLM responses with relevant context from the knowledge base

### Frontend
- **React 19**: Modern UI library for building the user interface
- **TypeScript**: Type-safe JavaScript for robust application development
- **Vite**: Next-generation frontend tooling for fast development and optimized builds
- **Tailwind CSS**: Utility-first CSS framework for custom styling

## 🏗️ Architecture

The application follows a client-server architecture:

1. **Text Processing Pipeline**:
   - PDF extraction and text cleaning of Sherlock Holmes stories
   - Text chunking and semantic classification (dialogue, narration, deduction)
   - Vector embedding generation and storage in ChromaDB

2. **RAG Query Processing**:
   - User queries are embedded and semantically matched with relevant text chunks
   - Retrieved context is used to augment the LLM prompt
   - Generated responses maintain character authenticity through contextual knowledge
   - Responses are streamed word-by-word to the frontend

## 🔗 Links

- **Live Application**: [Sherlock Holmes Detective Chatbot](https://sherlockbot.onrender.com)
- **API Endpoint**: [Sherlock Holmes API](https://sherlockbot.onrender.com/api)

## 🚀 Getting Started

### Prerequisites
- Python 3.9+
- Node.js and npm
- API key for Mistral AI

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/sherlock-bot.git
   cd sherlock-bot
   ```

2. Set up environment variables:
   Create a `.env` file in the `api` directory with your Mistral AI API key:
   ```
   API_KEY=your_mistral_ai_api_key
   ```

3. Install backend dependencies:
   ```bash
   cd api
   pip install -r requirements.txt
   ```

4. Install frontend dependencies:
   ```bash
   cd frontend
   npm install
   ```

5. Start the backend server:
   ```bash
   cd api
   uvicorn main:app --host 0.0.0.0 --port 8000
   ```

6. Start the frontend development server:
   ```bash
   cd frontend
   npm run dev
   ```

7. Access the application:
   Open your browser and navigate to the URL shown in your terminal (typically `http://localhost:5173`)

## 💻 Development

### Backend Development
```bash
cd api
pip install -r requirements.txt
uvicorn main:app --reload
```

### Frontend Development
```bash
cd frontend
npm install
npm run dev
```

## 🔒 Security Notes

- API keys should be kept secure and not committed to version control
- The application uses CORS with appropriate restrictions for API access

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgements

- Sir Arthur Conan Doyle for creating the timeless character of Sherlock Holmes
- Mistral AI for providing the language model capabilities
- All contributors and maintainers of the open-source libraries used in this project
```