# 🧠 AI-Powered Research Paper Summarizer

This project is a simple Streamlit-based AI application that helps users understand popular research papers in different styles and detail levels using Google's Gemini model through LangChain. It takes a research paper name, explanation style, and desired length as input and returns a tailored explanation.

---

## 🚀 Features

- 📄 Choose from popular AI research papers like **BERT**, **GPT-3**, **Attention is All You Need**, and **Diffusion Models Beat GANs**.
- 🎓 Select the **explanation style**: Beginner-Friendly, Technical, Code-Oriented, or Mathematical.
- 📏 Choose the **length of explanation**: Short (1-2 paragraphs), Medium (3-5 paragraphs), or Long (detailed explanation).
- 🤖 Utilizes **LangChain** with **Google's Gemini (via ChatGoogleGenerativeAI)** to generate accurate, styled responses.
- 💻 Simple and elegant UI built with **Streamlit**.

---

## 🛠️ Tech Stack

| Tool/Library           | Purpose                                  |
|------------------------|------------------------------------------|
| Python                 | Core programming language                |
| Streamlit              | Front-end UI                             |
| LangChain              | LLM orchestration and prompt templating  |
| Google Generative AI   | LLM backend (Gemini Pro)                 |
| dotenv                 | Manage API keys and environment configs  |

---

## 🔧 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/research-summarizer.git
cd research-summarizer

2. Install Dependencies

Make sure you have Python 3.10+ installed.

pip install -r requirements.txt

3. Set Up Environment Variables

Create a .env file in the root directory:

GOOGLE_API_KEY=your_google_generative_ai_key

    🔐 Never share your API key publicly.

4.1. Run prompt_generator.py

4.2. Run the App

streamlit run prompt_ui.py

📌 Notes on template.json

This file should be a LangChain-compatible prompt template. Example format:

{
  "input_variables": ["paper_input", "style_input", "length_input"],
  "template": "Explain the paper '{paper_input}' in a {style_input} style with {length_input} explanation."
}

This dynamic template allows the LLM to adjust tone and complexity based on user selections.
❓ Example Use Case

    A user selects:

        Paper: "GPT-3: Language Models are Few-Shot Learners"

        Style: "Beginner-Friendly"

        Length: "Short"

    The system returns:

        "GPT-3 is a very large AI model trained on a lot of text. It can perform many tasks without needing lots of training examples..."


🧪 .env.example

GOOGLE_API_KEY=your_google_api_key_here
