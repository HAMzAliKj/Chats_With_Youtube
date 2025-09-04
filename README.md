CHAT WIIH YOUTUBE | SUMMARIZER 
A lightweight toolkit to chat with YouTube videos — ask questions, get concise summaries, and explore video content using an LLM + RAG pipeline fed by YouTube transcripts.

What it does

Downloads a video's transcript (YouTube Transcript API / captions).

Splits and embeds transcript chunks into a vector store.

Uses Retrieval-Augmented Generation (RAG) to answer user questions with context from the video.

Produces short summaries, timestamps, and direct quotes from the transcript.

Built to be simple to run locally or deploy (Procfile included).

Key features

✅ Ask anything about a YouTube video (topic, details, quotes, timestamps).

✅ Automatic summarization (short, medium, long).

✅ RAG-backed answers so the LLM cites transcript context.

✅ Extensible — swap LLMs, vector DBs, or transcript sources easily.

High-level architecture

YouTube Transcript API → fetch captions / transcript for a video ID / URL.

Text splitter → break transcript into chunks (preserve short context + timestamps).

Embeddings → convert chunks into vectors (OpenAI / other embedding model).

Vector store → FAISS / Chroma / Pinecone (local or cloud) to store and search chunks.

Retriever + LLM → retrieve top-k chunks for a query, pass to LLM to synthesize an answer (RAG).

Output → answer, short summary, highlighted transcript snippets with timestamps.

Quickstart (recommended)

Example assumes Python and the repository layout includes check.py and requirements.txt.

Clone the repo:

git clone https://github.com/HAMzAliKj/Chats_With_Youtube.git
cd Chats_With_Youtube


Create a virtual environment and install:

python -m venv .venv
source .venv/bin/activate   # macOS / Linux
.venv\Scripts\activate      # Windows
pip install -r requirements.txt
