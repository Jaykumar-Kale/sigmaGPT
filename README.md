# SigmaGPT

A full-stack MERN-based ChatGPT replica built from scratch with OpenAI integration. This application demonstrates modern web development practices with a responsive React frontend and a Node.js/Express backend.

## Overview

SigmaGPT is a conversational AI application that integrates OpenAI's API to provide intelligent chat capabilities. Built with the MERN stack (MongoDB, Express, React, Node.js), this project showcases a complete implementation of a real-time chat application with message persistence and conversation management.

## Features

- Real-time chat interface with OpenAI integration
- Conversation history and thread management
- Responsive and intuitive user interface
- RESTful API backend with Express.js
- Database persistence with MongoDB
- Environment-based configuration

## Tech Stack

**Frontend:**

- React 18
- Vite (build tool)
- CSS3 for styling
- Context API for state management

**Backend:**

- Node.js
- Express.js
- MongoDB
- OpenAI API

**Development Tools:**

- ESLint for code quality
- npm for package management

## Project Structure

```
sigmaGPT/
├── Backend/
│   ├── models/
│   │   └── Thread.js          # MongoDB Thread schema
│   ├── routes/
│   │   └── chat.js            # Chat endpoints
│   ├── utils/
│   │   └── openai.js          # OpenAI API integration
│   ├── server.js              # Express server entry point
│   ├── package.json           # Backend dependencies
│   └── package-lock.json
├── Frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── App.jsx        # Main component
│   │   │   ├── Chat.jsx       # Chat interface
│   │   │   ├── ChatWindow.jsx # Message display
│   │   │   ├── Sidebar.jsx    # Navigation sidebar
│   │   │   └── MyContext.jsx  # Context provider
│   │   ├── assets/            # Images and static files
│   │   ├── main.jsx           # React entry point
│   │   └── index.css          # Global styles
│   ├── public/                # Static public files
│   ├── index.html             # HTML template
│   ├── vite.config.js         # Vite configuration
│   ├── package.json           # Frontend dependencies
│   └── eslint.config.js       # ESLint configuration
├── README.md
└── .gitignore
```

## Installation

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- MongoDB instance
- OpenAI API key

### Backend Setup

1. Navigate to the Backend directory:

   ```bash
   cd Backend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the Backend directory with required environment variables:

   ```
   OPENAI_API_KEY=your_openai_api_key
   MONGODB_URI=your_mongodb_connection_string
   PORT=5000
   ```

4. Start the backend server:
   ```bash
   npm start
   ```

### Frontend Setup

1. Navigate to the Frontend directory:

   ```bash
   cd Frontend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the Frontend directory if needed:

   ```
   VITE_API_URL=http://localhost:5000
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

## Usage

1. Open your browser and navigate to `http://localhost:5173` (default Vite port)
2. Start a new conversation in the chat interface
3. Type your message and submit to interact with the ChatGPT replica
4. Conversations are automatically saved to the database

## API Endpoints

### Chat Routes (`/api/chat`)

- `POST /chat` - Send a message and receive a response
- `GET /threads` - Retrieve conversation history
- `GET /threads/:id` - Get a specific thread
- `DELETE /threads/:id` - Delete a conversation thread

## Configuration

### Environment Variables

**Backend .env:**

- `OPENAI_API_KEY` - Your OpenAI API key
- `MONGODB_URI` - MongoDB connection string
- `PORT` - Server port (default: 5000)

**Frontend .env:**

- `VITE_API_URL` - Backend API URL

## Development

### Running in Development Mode

**Terminal 1 - Backend:**

```bash
cd Backend
npm start
```

**Terminal 2 - Frontend:**

```bash
cd Frontend
npm run dev
```

### Code Quality

Lint the Frontend code:

```bash
cd Frontend
npm run lint
```

## Building for Production

### Frontend Build

```bash
cd Frontend
npm run build
```

The built files will be in the `dist/` directory.

## File Guidelines

- Ensure `.env` files are never committed (included in `.gitignore`)
- `node_modules/` directories are excluded from version control
- macOS system files (`.DS_Store`) are ignored

## Future Enhancements

- User authentication and authorization
- Conversation sharing capabilities
- Multiple AI model support
- Advanced conversation search and filtering
- Conversation export functionality
- Custom system prompts

## Contributing

This is a personal project. For improvements or modifications, fork the repository and submit pull requests.

## License

This project is open source and available under the MIT License.

## Support

For questions or issues, please create an issue in the repository or contact the project maintainer.

---

**Last Updated:** April 2026
