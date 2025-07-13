# 🔍 SEO Keyword Research Agent (n8n Workflow)

This project is an **AI-powered keyword research automation** built with [n8n](https://n8n.io/). It takes a **seed keyword** as input and returns **50 highly relevant SEO keyword suggestions**, optimized to help content rank on the first page of Google.

---

## 🚀 How It Works

1. **User Input via Chat**  
   Enter a single **seed keyword** in the chat interface (e.g., `collabora online`).

2. **Google Autocomplete API (SerpAPI)**  
   The workflow makes a real-time HTTP request to [SerpAPI](https://serpapi.com/) to fetch Google Autocomplete suggestions for that keyword.

3. **Extract Suggestions**  
   All autocomplete suggestions are cleaned and transformed into a usable text block.

4. **AI Agent Keyword Generation**  
   Using `OpenRouter` + `Gemini` integration, an AI agent processes the suggestions and generates **50 strategic keywords** that are:
   - Closely related to the seed keyword
   - High in search volume
   - Low in competition
   - Include long-tail, high-intent phrases
   - Suitable for content marketing

5. **Structured Output**  
   The generated keywords are formatted into:
   - A `.json` file for further use
   - A clean Markdown table showing keyword + intent

---

## 📦 Output Format

Each keyword in the output includes:
```json
{
  "keyword": "collabora online for schools",
  "intent": "informational"
}
```

## File Generation

The keyword suggestions are saved as a downloadable .json file and returned as a formatted table inside the n8n chat window.