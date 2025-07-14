# research-agent-llm

> A pydantic‑structured, multi‑LLM research assistant agent that uses web search and Wikipedia tools.

## 🚀 Features

- 🔎 Conducts web searches via DuckDuckGo.
- 📚 Pulls targeted summaries from Wikipedia.
- 🧩 Parses outputs into a well‑defined Pydantic model (`ResearchResponse`).
- 💾 Optional “save to file” tool for archiving results with timestamps.
- 🔄 Easily swap in different LLMs (OpenAI, Anthropic, etc.).

## 🛠️ Tech Stack

- **Python 3.10+**  
- **[LangChain](https://github.com/langchain-ai/langchain)** for agent orchestration  
- **Pydantic** for structured outputs  
- **python‑dotenv** for config management  
- **DuckDuckGoSearchRun** and **WikipediaAPIWrapper** tools  

## 📦 Installation

1. Clone the repo  
   ```bash
   git clone https://github.com/your‑username/research-agent-llm.git
   cd research-agent-llm
Create & activate your virtual environment

python3 -m venv .venv
source .venv/bin/activate
Install dependencies

pip install -r requirements.txt
🔧 Configuration
Copy .env.example to .env

Fill in your keys:

OPENAI_API_KEY=your_openai_key
ANTHROPIC_API_KEY=your_claude_key
🎯 Usage
python main.py
You’ll be prompted:

What can I help you research?
Enter your topic and let the agent fetch, parse, and display a structured summary.

Example
> What can I help you research?  
  Topic: “Quantum computing error correction”
  
# Output:
topic: "Quantum computing error correction"
summary: "Error correction in quantum computing..."
sources:
  - "https://en.wikipedia.org/..."
tools_used:
  - "search_tool"
  - "wiki_tool"
📁 Project Structure
.
├── main.py            # entrypoint with AgentExecutor
├── tools.py           # search, wiki and save‑to‑file tools
├── models.py          # Pydantic ResearchResponse
├── requirements.txt
├── .env.example
└── README.md
🤝 Contributing
Fork the repo

Create your feature branch (git checkout -b feature/XYZ)

Commit your changes (git commit -m 'Add XYZ')

Push to branch (git push origin feature/XYZ)

Open a Pull Request

📄 License
This project is licensed under the MIT License. See LICENSE for details.

Feel free to tweak sections (add badges, CI instructions, etc.) to suit your style.