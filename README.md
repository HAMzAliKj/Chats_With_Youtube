🎥 Chat with YouTube | Summarizer


A lightweight toolkit to chat with YouTube videos — ask questions, get concise summaries, and explore video content using an LLM + RAG pipeline powered by YouTube transcripts.

🔹 What it does

📥 Downloads a video's transcript (YouTube Transcript API / captions).
✂️ Splits and embeds transcript chunks into a vector store.
🤖 Uses Retrieval-Augmented Generation (RAG) to answer user questions with transcript context.
📝 Produces short summaries, timestamps, and direct transcript quotes.
⚡ Simple to run locally or deploy (Procfile included).

🌟 Key Features

✅ Ask anything about a YouTube video (topics, details, quotes, timestamps).
✅ Automatic summarization (short, medium, long).
✅ RAG-backed answers — responses cite transcript context.
✅ Extensible — swap LLMs, vector DBs, or transcript sources easily.

🏗️ High-Level Architecture

YouTube Transcript API → fetch captions/transcript for a video ID / URL.
Text splitter → chunk transcript while preserving context & timestamps.
Embeddings → convert chunks into vectors (OpenAI / other models).
Vector store → FAISS / Chroma / Pinecone (local or cloud).
Retriever + LLM → retrieve top-k chunks, feed into LLM for synthesis (RAG).
Output → concise answer + summary + transcript snippets with timestamps.

🚀 Quickstart

Example assumes Python and repo includes check.py + requirements.txt.

1️⃣ Clone the repo:
git clone https://github.com/HAMzAliKj/Chats_With_Youtube.git
cd Chats_With_Youtube

2️⃣ Create a virtual environment & install dependencies:
python -m venv .venv
source .venv/bin/activate   # macOS / Linux
.venv\Scripts\activate      # Windows
pip install -r requirements.txt
