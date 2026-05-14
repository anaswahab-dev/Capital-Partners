# AI Chat App

A modern AI chat application built with React and OpenAI integration.

## Features

- 💬 **Real-time Messaging**: Seamless chat interface with instant message delivery
- 📚 **Multiple Conversations**: Create and manage multiple chat conversations simultaneously
- 💾 **Chat History Persistence**: All conversations are automatically saved to browser storage
- 🎨 **Modern UI**: Clean and intuitive interface built with React and Tailwind CSS
- 🔐 **State Management**: Zustand for efficient and scalable state management
- 🚀 **Fast Performance**: Vite for lightning-fast development and production builds

## Tech Stack

### Frontend
- **React 18.2** - UI library
- **Vite** - Build tool and development server
- **Tailwind CSS** - Utility-first CSS framework
- **Zustand** - State management
- **React Icons** - Icon library
- **date-fns** - Date formatting
- **Axios** - HTTP client

### Backend
- **Node.js** - Runtime
- **Express** - Web framework
- **OpenAI API** - AI integration
- **CORS** - Cross-origin resource sharing

## Prerequisites

Before getting started, make sure you have:
- Node.js 16+ installed
- An OpenAI API key (get one at https://platform.openai.com/api-keys)

## Installation

1. **Clone the repository**
```bash
git clone https://github.com/anaswahab-dev/Capital-Partners.git
cd Capital-Partners/ai-chat-app
```

2. **Install dependencies**
```bash
npm install
```

3. **Create environment file**
```bash
cp .env.example .env.local
```

4. **Add your OpenAI API key**
```
OPENAI_API_KEY=your_api_key_here
```

## Running the Application

### Development Mode

**Terminal 1 - Frontend (Vite)**
```bash
npm run dev
```
This starts the Vite dev server at `http://localhost:5173`

**Terminal 2 - Backend (Express)**
```bash
npm run server
```
This starts the Express server at `http://localhost:3001`

### Production Build

```bash
npm run build
npm run preview
```

## Project Structure

```
ai-chat-app/
├── src/
│   ├── components/
│   │   ├── ChatWindow.jsx      # Main chat interface
│   │   ├── ChatWindow.css
│   │   ├── Sidebar.jsx         # Conversation list sidebar
│   │   ├── Sidebar.css
│   │   ├── MessageBubble.jsx   # Individual message component
│   │   └── MessageBubble.css
│   ├── store/
│   │   └── chatStore.js        # Zustand chat store
│   ├── App.jsx                 # Main app component
│   ├── App.css
│   ├── main.jsx                # React entry point
│   └── index.css               # Global styles
├── server/
│   └── index.js                # Express backend
├── index.html                  # HTML entry point
├── package.json                # Dependencies
├── vite.config.js              # Vite configuration
├── tailwind.config.js          # Tailwind configuration
└── .env.example                # Environment template
```

## Key Features Explained

### 1. **Real-time Messaging**
Messages are displayed instantly as you type and send. The UI smoothly animates new messages and auto-scrolls to the latest.

### 2. **Multiple Conversations**
- Create unlimited conversations with the "New Chat" button
- Switch between conversations instantly
- Each conversation maintains its own message history
- Conversations are sorted by last updated time

### 3. **Chat History Persistence**
- All conversations are automatically saved to browser's localStorage
- Data persists across browser sessions
- Delete conversations you no longer need

### 4. **Zustand State Management**
The `chatStore` provides:
- Conversation CRUD operations
- Message management
- Current conversation tracking
- Persistent storage with localStorage middleware

## Environment Variables

Create a `.env.local` file in the root directory:

```env
OPENAI_API_KEY=sk-your-api-key-here
VITE_API_URL=http://localhost:3001
```

## API Endpoints

### POST /chat
Sends a message to OpenAI and returns the response.

**Request:**
```json
{
  "messages": [
    {
      "role": "user",
      "content": "Hello, how are you?"
    }
  ]
}
```

**Response:**
```json
{
  "message": "I'm doing great, thanks for asking!",
  "usage": {
    "prompt_tokens": 10,
    "completion_tokens": 15,
    "total_tokens": 25
  }
}
```

## Troubleshooting

### Port Already in Use
If port 3001 or 5173 is already in use:
```bash
# Change port in package.json or use:
PORT=3002 npm run server
```

### API Key Issues
- Verify your OpenAI API key is valid
- Check that you have API credits available
- Ensure `.env.local` file is in the correct directory

### CORS Errors
Make sure the backend server is running on `http://localhost:3001`

## Future Enhancements

- [ ] User authentication
- [ ] Message editing and deletion
- [ ] Typing indicators
- [ ] File upload support
- [ ] Conversation search
- [ ] Dark mode
- [ ] Export conversations
- [ ] Real-time collaboration
- [ ] Voice input/output
- [ ] Multiple AI model support

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the MIT License.

## Support

For issues and questions, please create an issue in the GitHub repository.

---

**Built with ❤️ using React + OpenAI**
