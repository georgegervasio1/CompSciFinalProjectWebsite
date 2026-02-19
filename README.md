# Client Analytics Portal

A secure web portal for analyzing client injury data with AI-powered insights using Tinker LLM.

## 🚀 Setup Instructions

### 1. Install Python Dependencies
```bash
pip install -r requirements.txt
```

### 2. Prepare Your Data
- Convert your JSON data to **clients.csv**
- Place `clients.csv` in the same folder as `app.py` and `index.html`

### 3. Start the Flask Server
```bash
python app.py
```

You should see:
```
🚀 Starting Flask server...
📊 Loading client data...
🤖 Tinker LLM ready

💻 Open http://localhost:5000 in your browser
```

### 4. Open in Browser
- Navigate to: **http://localhost:5000**
- Login password: `final2026`

## 📁 File Structure

```
your-project/
├── app.py              # Flask backend (connects to Tinker LLM)
├── index.html          # Frontend interface
├── clients.csv         # Your client data
├── requirements.txt    # Python dependencies
└── README.md          # This file
```

## ✨ Features

### View Client Data Tab
- **Search bar** - Find clients by any field
- **Advanced filters**:
  - Filter by State
  - Filter by Year
  - Filter by Brand
  - Clear all filters button
- **Client cards** with expandable details
- **Statistics** - Total clients and filtered count

### Data Analysis Tab
- **AI Chat Interface** - Ask questions about your data
- Powered by **Tinker LLM** (Llama-3.1-8B-Instruct)
- Connected to your Python code
- Real-time data analysis

## 💬 Example Questions to Ask the AI

- "How many clients are from California?"
- "What are the most common injury types?"
- "Which brands were used most frequently?"
- "Show me trends by state"
- "What's the average incident date?"

## 🔧 How It Works

1. **Frontend (index.html)** - Beautiful UI with Bridge Legal styling
2. **Backend (app.py)** - Flask server that:
   - Serves the HTML and CSV files
   - Connects to your Tinker LLM Python code
   - Processes chat requests through `/api/chat` endpoint
3. **Your LLM Code** - Runs exactly as you wrote it in the chat endpoint

## 🐛 Troubleshooting

### "Could not load client data"
- Make sure Flask server is running: `python app.py`
- Check that `clients.csv` exists in the same folder
- Refresh the browser page

### "Could not connect to AI service"
- Verify Flask server is running on port 5000
- Check console for errors: `python app.py`
- Make sure your Tinker API key is valid

### Port already in use
```bash
# Use a different port
python app.py  # Edit line in app.py: app.run(port=5001)
```

## 🎨 Customization

- **Change password**: Edit line in `index.html` and `app.py`
- **Adjust LLM settings**: Modify `max_tokens` and `temperature` in `app.py`
- **Update styling**: Edit CSS in `index.html`

## 📝 Notes

- The LLM has access to a summary of your data
- Temperature is set to 0.5 for consistent responses
- Max tokens is 200 (increase for longer responses)
- CORS is enabled for local development
