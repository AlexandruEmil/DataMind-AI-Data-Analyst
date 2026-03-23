# DataMind — AI Data Analyst 🧠

> Upload a CSV or Excel file, ask questions in plain English, and get instant charts, SQL queries, Pandas code, and AI-powered insights — completely free.

![Made with HTML](https://img.shields.io/badge/Made%20with-HTML%20%2B%20JS-00e5a0?style=flat-square)
![AI Powered](https://img.shields.io/badge/AI-LLaMA%203.3%2070B-7c5cfc?style=flat-square)
![Free](https://img.shields.io/badge/Cost-%240%2Fmonth-00e5a0?style=flat-square)
![No Backend](https://img.shields.io/badge/Backend-None-ff5e7d?style=flat-square)

---

## What It Does

DataMind lets anyone — technical or not — have a conversation with their data.

- **Upload** a CSV or Excel file (drag & drop supported)
- **Ask anything** in plain English: *"What are the top trends?"*, *"Which salesperson made the most revenue?"*, *"Show me anomalies"*
- **Get back:**
  - 📊 Auto-generated charts (bar, line, pie — switchable)
  - 💡 Key insights highlighted in callout blocks
  - 🗄️ Ready-to-run SQL queries
  - 🐍 Copy-paste Pandas code for Jupyter
  - 💬 Clear natural language explanations

---

## Demo

| Step | What happens |
|------|-------------|
| 1. Drop a CSV | Columns parsed instantly, chart auto-rendered |
| 2. Ask a question | *"Which region had the highest sales in Q3?"* |
| 3. Get the answer | Insight block + SQL + chart update |

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| AI Model | LLaMA 3.3 70B via [Groq API](https://groq.com) (free tier) |
| File Parsing | [PapaParse](https://www.papaparse.com/) (CSV) + [SheetJS](https://sheetjs.com/) (Excel) |
| Charts | [Chart.js 4](https://www.chartjs.org/) |
| Frontend | Vanilla HTML + JavaScript — zero frameworks |
| Deployment | Single `.html` file — runs anywhere |

No backend. No database. No server costs.

---

## Getting Started

### 1. Get a free Groq API key

Go to [console.groq.com/keys](https://console.groq.com/keys), create a free account (no credit card required), and generate an API key.

### 2. Open the app

Download `datamind.html` and open it in any modern browser. Or host it for free on:
- [GitHub Pages](https://pages.github.com/)
- [Netlify Drop](https://app.netlify.com/drop)
- [Vercel](https://vercel.com/)

### 3. Start analysing

1. Paste your Groq API key in the sidebar
2. Upload a CSV or Excel file
3. Ask your first question

---

## Project Structure

```
datamind.html       ← The entire app (single file)
vanzari_test.csv    ← Sample dataset (500 rows) for testing
README.md           ← This file
```

Everything lives in one HTML file. No `npm install`, no build step, no config.

---

## Sample Questions to Try

Once you load `vanzari_test.csv` (the included sample dataset):

```
"What are the top trends in this data?"
"Which salesperson generated the most revenue?"
"Show me a statistical summary of all numeric columns"
"Which region had the highest number of sales?"
"Generate a SQL query to find the top 10 transactions by revenue"
"Write Pandas code to group sales by category and month"
"Are there any anomalies or outliers in the data?"
"Predict the trend for next month based on the existing data"
```

---

## Features

### Multi-turn conversation
DataMind remembers the full conversation history, so you can ask follow-up questions naturally:
> *"Which product sold the most?"* → *"And which region did it sell best in?"* → *"Generate SQL for that"*

### Auto chart rendering
When a file is loaded, a chart is generated automatically from the first numeric column. Switch between bar, line, and pie with one click.

### SQL & Pandas output
Every analytical question can produce:
- A SQL query (for any SQL database)
- A Pandas snippet (ready for Jupyter Notebook or VS Code)

### Works offline (after first load)
Once the page is loaded, only the AI API calls require internet. File parsing and chart rendering work fully offline.

---

## Limitations

- **API rate limits**: Groq's free tier allows ~30 requests/minute. For heavy usage, check their [rate limit docs](https://console.groq.com/docs/rate-limits).
- **File size**: Large files (100k+ rows) are sampled to the first 60 rows when sent to the AI. All rows are used for local charts.
- **No data persistence**: Data is not saved between sessions. Refresh = start over.
- **Browser only**: No server-side processing — everything runs in your browser tab.

---

## Skills Demonstrated

This project was built to demonstrate practical data engineering and AI integration skills:

- **API Integration** — Connected a third-party LLM API with auth, error handling, and conversation state management
- **Data Pipeline** — Built a browser-side ETL: file upload → parsing → type detection → transformation → visualisation
- **Prompt Engineering** — Structured system prompts to reliably produce SQL, Pandas, and insight blocks in a consistent format
- **UX Design** — Designed for non-technical users: quick-prompt buttons, auto-charts, highlighted insights
- **Zero-dependency Architecture** — Delivered a production-grade tool with no build tooling, no framework, no backend

---

## Local Development

Since this is a single HTML file, there's no build process:

```bash
# Clone the repo
git clone https://github.com/yourusername/datamind.git
cd datamind

# Open in browser
open datamind.html          # macOS
start datamind.html         # Windows
xdg-open datamind.html      # Linux
```

For live reload during development:

```bash
# Using Python's built-in server
python3 -m http.server 8080
# Then open http://localhost:8080/datamind.html
```

---

## Contributing

Pull requests are welcome. For major changes, please open an issue first.

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/add-export`)
3. Commit your changes (`git commit -m 'Add CSV export button'`)
4. Push to the branch (`git push origin feature/add-export`)
5. Open a Pull Request

---

## License

MIT — free to use, modify, and distribute.

---

## Author

Built by **[Your Name]** as a portfolio project.

- 🔗 [LinkedIn](https://linkedin.com/in/yourprofile)
- 💻 [GitHub](https://github.com/yourusername)
- 📧 your.email@example.com

---

*If this project helped you or gave you ideas, consider leaving a ⭐ — it helps others find it.*
