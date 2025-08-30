🤖 LLM Agent UI

A sleek, powerful, and browser-based UI for interacting with OpenAI-compatible Large Language Models. This proof-of-concept application is designed for developers and enthusiasts to experiment with LLM agents that can execute tools, all within a clean and intuitive interface.
✨ Key Features

    🔌 OpenAI-Compatible: Connect to any service that exposes an OpenAI-compatible /v1/chat/completions endpoint, including custom servers or providers like AiPipe.

    🛠️ Powerful Tool Integration: Comes pre-configured with three essential tools:

        Google Search: Perform real-time Google searches.

        aipipe_run: Execute complex workflows via an AiPipe proxy.

        run_js: Run JavaScript code in a secure, sandboxed Worker environment.

    ⚙️ Persistent Configuration: Your settings for providers, models, API keys, and endpoints are automatically saved to your browser's local storage.

    📊 Detailed Logging: A collapsible logs drawer provides a real-time, detailed view of every request, response, tool call, and error, making debugging a breeze.

    🎨 Modern & Responsive UI: A clean, minimalistic interface with high-contrast elements that looks great on any device.

    🚀 Zero Backend Required: Runs entirely in the browser as a static web application.

🛠️ Technology Stack

    Frontend: HTML5, CSS3, Vanilla JavaScript

    Styling: Bootstrap 5

    Server: http-server (for local development)

🚀 Getting Started

Follow these instructions to get the project up and running on your local machine.
Prerequisites

    Node.js (which includes npm)

Installation & Running

    Clone the repository:

    git clone [https://github.com/your-username/llm-agent.git](https://github.com/your-username/llm-agent.git)
    cd llm-agent

    Install dependencies:

    npm install

    Start the local development server:

    npm start

    The application will now be running and accessible at http://localhost:8080 (or another port if 8080 is in use).

⚙️ Configuration

The UI allows you to configure the following settings:

Field
	

Description

Provider
	

Select a pre-configured provider (AiPipe, OpenAI-compatible) or Custom.

Model
	

Select the LLM model to use from the dropdown. The list is populated based on the chosen provider.

Base URL
	

The base URL of the OpenAI-compatible API endpoint.

API Key
	

Your secret API key for the service. This is stored locally and never leaves your browser.

Google Key & CX
	

Your API Key and Custom Search Engine ID for using the Google Search tool.

AiPipe Endpoint
	

The endpoint URL for the aipipe_run tool.

Max loops
	

The maximum number of agent-tool iterations to prevent infinite loops. Defaults to 6.

    Tip: Use the "Test credentials" button to verify that your Base URL and API Key are working correctly by fetching the available models.

🔧 Tool Reference

To use a tool, simply ask the agent to perform a task that requires it. For example: "search for the latest news on AI".

Tool Name
	

Description
	

Parameters

Google Search
	

Returns snippet results from a Google CSE search.
	

query (string), num (integer, optional, default: 5)

aipipe_run
	

Calls an AiPipe proxy with a specified flow.
	

flow (string), payload (object), endpoint (string, optional)

run_js
	

Executes JavaScript code in a sandboxed Worker.
	

code (string), timeout_ms (integer, optional, default: 2000)
☁️ Deployment

This application is a static site and can be deployed to any static hosting provider. The included Procfile is configured for one-click deployment to services like Heroku.

web: npx http-server . -p $PORT

📄 License

This project is licensed under the MIT License. See the LICENSE file for details.