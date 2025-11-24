# Inceptus

Inceptus, derived from the Latin word for “the beginning,” is a generative AI-powered web application that allows you to describe a website you want to build, and it will generate the code for you in real-time. You can then interact with the AI to further refine and develop your application.

## How it Works

1.  **Describe Your Idea:** You start by providing a prompt that describes the website you want to build.
2.  **AI-Powered Scaffolding:** Inceptus sends your prompt to a backend service powered by Google's Gemini model. The backend determines the appropriate stack (React or Node.js) and generates the initial set of files and code.
3.  **In-Browser Development:** The generated files are mounted into a WebContainer, an in-browser Node.js environment. This allows you to see a live preview of your application directly in your browser.
4.  **Real-time Editing and Preview:** The application provides a VS Code-like experience with a file explorer, a code editor (Monaco Editor), and a live preview. You can edit the generated code and see the changes reflected in the preview instantly.
5.  **Iterative Development:** You can continue to provide prompts and instructions to the AI to add new features, modify existing ones, or fix bugs. The AI will generate the necessary code changes, which you can review and apply.

## Features

-   **Generative AI:** Uses Google's Gemini model to generate code from natural language prompts.
-   **In-Browser Development Environment:** Runs a full Node.js environment in the browser using WebContainers.
-   **Live Preview:** See your application come to life as the AI generates the code.
-   **File Explorer:** Navigate the file structure of your generated project.
-   **Code Editor:** A feature-rich code editor based on Monaco Editor.
-   **Iterative Building:** Continue to work with the AI to build and refine your application.

## Technologies Used

**Frontend:**

-   [React](https://reactjs.org/)
-   [Vite](https://vitejs.dev/)
-   [Tailwind CSS](https://tailwindcss.com/)
-   [Monaco Editor](https://microsoft.github.io/monaco-editor/)
-   [WebContainer API](https://webcontainers.io/)
-   [TypeScript](https://www.typescriptlang.org/)

**Backend:**

-   [Node.js](https://nodejs.org/)
-   [Express](https://expressjs.com/)
-   [Google Gemini API](https://ai.google.dev/)
-   [TypeScript](https://www.typescriptlang.org/)

## Getting Started

### Prerequisites

-   [Node.js](https://nodejs.org/en/download/) (v18 or higher recommended)
-   A [Google Gemini API Key](https://ai.google.dev/)

### Installation and Running

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/S-hub18/inceptus1.git
    cd inceptus
    ```

2.  **Backend Setup:**
    ```bash
    cd backend
    npm install
    ```
    Create a `.env` file in the `backend` directory and add your Gemini API key:
    ```
    GEMINI_API_KEY=your_api_key
    ```
    Start the backend server:
    ```bash
    npm run dev
    ```

3.  **Frontend Setup:**
    In a new terminal, navigate to the `frontend` directory:
    ```bash
    cd frontend
    npm install
    npm run dev
    ```

4.  **Open the application:**
    Open your browser and navigate to `http://localhost:5173` (or the port specified by Vite).

## Project Structure

```
.
├── backend/                # Node.js backend
│   ├── src/
│   │   ├── index.ts        # Main server file
│   │   ├── prompts.ts      # Prompts for the AI model
│   │   └── defaults/       # Default project templates
│   ├── package.json
│   └── tsconfig.json
└── frontend/               # React frontend
    ├── src/
    │   ├── components/     # React components
    │   ├── hooks/          # Custom React hooks
    │   ├── pages/          # Page components (Home, Builder)
    │   ├── App.tsx         # Main application component
    │   └── main.tsx        # Entry point
    ├── package.json
    └── vite.config.ts
```
