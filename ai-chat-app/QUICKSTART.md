# Quick Start Guide

## Prerequisites
- Node.js 16+
- OpenAI API Key

## 5-Minute Setup

### 1. Install Dependencies
```bash
npm install
```

### 2. Setup Environment
```bash
cp .env.example .env.local
```

Then edit `.env.local` and add your OpenAI API key:
```
OPENAI_API_KEY=sk-your-actual-api-key-here
```

**Get your API key:** https://platform.openai.com/api-keys

### 3. Start the Application

**Option A: Run both services (recommended)**
```bash
npm run dev:all
```

**Option B: Run separately in two terminals**

Terminal 1 - Frontend:
```bash
npm run dev
```

Terminal 2 - Backend:
```bash
npm run server
```

### 4. Open in Browser
Visit `http://localhost:5173`

## Common Issues

### Port Already in Use
```bash
# Change port in terminal
PORT=3002 npm run server
```

### API Key Error
- Verify key is in `.env.local`
- Check key is valid at https://platform.openai.com/api-keys
- Ensure you have API credits

### CORS Errors
- Make sure backend is running on `http://localhost:3001`
- Check frontend is accessing correct API URL

## Next Steps

1. ✅ Create a new conversation
2. ✅ Send a message to AI
3. ✅ Switch between conversations
4. ✅ Delete old conversations

## Tips

- Messages auto-save to browser storage
- Conversations sorted by most recent
- Click the trash icon to delete a conversation
- Click the + button to create new chat

Enjoy your AI Chat App! 🚀
