 Permission Query Assistant

This is a Streamlit-based AI assistant that helps users query an access control Excel file and answer general knowledge questions using an offline Mistral language model. It supports natural language queries, semantic search, rule-based permission dependency validation, and offline reasoning with Mistral GGUF.


  Features
- ✅ Semantic search using Sentence Transformers + FAISS
- ✅ Permission dependency validation logic (e.g., "Can I give Modify permission?")
- ✅ Queries for unique values, counts, filters from Excel
- ✅ General natural language Q&A using offline Mistral LLM (GGUF)
- ✅ Light/Dark mode UI toggle
- ✅ Session history for previous queries


  Folder Structure
.
├── .streamlit/
│   └── secrets.toml              # Optional: Hugging Face token or config
├── src/
│   ├── streamlit_app.py          # Streamlit UI logic
│   ├── rag_excel_bot.py          # Core backend logic
│   └── mistral_inference.py      # Wrapper for local Mistral model (GGUF)
├── permissions.xlsx              # Excel file containing permission data
├── requirements.txt              # List of Python packages
└── README.md                     # You're reading it!


 How to Clone and Run from GitHub

 1. Clone the repository

git clone https://github.com/Buddingbuddies25/rag_bot.git
cd rag_bot

 2. Set up the environment

python -m venv rag_env
source rag_env/bin/activate       # Windows: rag_env\Scripts\activate

 3. Install packages

pip install -r requirements.txt

 4. Run the app

streamlit run src/streamlit_app.py

 Example Queries

 General Questions
- `How many legs does a cat have?`
- `What is artificial intelligence?`

 Excel-Based Permission Queries
- `Can I give Download permission?`
- `Unique values in Site subtype`
- `How many entries have Modify permission?`
- `Show all entries for site 'Accenture /Default'`
- `Who are the unique groups?`

 Tech Stack

- [Streamlit](https://streamlit.io/)
- [Transformers](https://huggingface.co/transformers/)
- [llama-cpp-python](https://github.com/abetlen/llama-cpp-python)
- [Sentence Transformers](https://www.sbert.net/)
- [FAISS](https://github.com/facebookresearch/faiss)

 Model Details

- Model Name: `mistral-7b-instruct-v0.1.Q4_K_M.gguf`
- Source: [Hugging Face Model Hub](https://huggingface.co/Buddingbuddies25/rag_bot)
- Format: GGUF for use with `llama-cpp-python`
