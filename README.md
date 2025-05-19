# 🤖 X AI Agent — Gemini 2.0-Powered Modular Agent Framework with MCP Server

**X AI Agent** is a powerful, modular, and extensible autonomous AI agent framework built using **JavaScript** and powered by **Gemini 2.0 Flash** via the **Model Context Protocol (MCP)**. It enables LLMs to interact with external tools, APIs, memory systems, and more through a structured and unified interface, allowing for flexible and scalable AI workflows.

---

## 🚀 Features

* 🧠 **Gemini 2.0 Flash LLM Integration**

  * Lightweight, fast, and efficient language model from Google.
  * Ideal for real-time tool use and agentic reasoning.

* 🔗 **Model Context Protocol (MCP)**

  * Standardized protocol for connecting LLMs with external tools.
  * Ensures consistent formatting of inputs, outputs, and tool schemas.

* 🧩 **Modular Tool System**

  * Plug-and-play architecture for adding tools like search, code, API calls, and more.
  * Tools communicate with the LLM via MCP-defined JSON schemas.

* ♻️ **Autonomous Agent Loop**

  * Based on ReAct and AutoGPT-style reasoning chains.
  * Supports reflection, planning, and iterative tool use.

* 💾 **Memory Integration**

  * Vector search memory using **ChromaDB** or **Weaviate**.
  * Stores past thoughts, actions, and tool responses for improved context.

* 🌐 **Web API Interface**

  * REST and WebSocket endpoints to expose the agent to frontend UIs or other services.

* 🔐 **Secure Tool Execution**

  * Controlled sandboxed environments to safely execute code and external tasks.

---

## 🧪 Tech Stack

| Layer               | Technology                     |
| ------------------- | ------------------------------ |
| Language Model      | Gemini 2.0 Flash (via API)     |
| Protocol Layer      | Model Context Protocol (MCP)   |
| Language            | JavaScript (Node.js)           |
| Web Framework       | Express.js (API endpoints)     |
| Memory System       | ChromaDB / Weaviate            |
| Tool Execution      | Custom JS-based tool runner    |
| Vector Embeddings   | Gemini Embeddings / OpenRouter |
| Frontend (optional) | React.js / Next.js (optional)  |

---

## 🛠️ Available Tools

* **search** – Web search using Exa/Bing/Google APIs
* **code** – JavaScript and Python sandboxed code execution
* **web** – Make external HTTP requests
* **memory** – Vector-based long-term recall system
* **fs** – Read and write local files (controlled access)
* **db** – Connect and query SQL/NoSQL databases

All tools follow the MCP tool schema and return structured responses.

---

## 🧠 Agent Architecture

```text
[ User ]
   ↓
[ Gemini 2.0 Flash LLM ] ←→ [ MCP Server ] ←→ [ Tools / Memory / APIs ]
```

* The LLM sends tool requests via MCP
* The MCP server handles routing, execution, and returns structured results
* The agent reflects and decides next steps iteratively

---

## 📦 Installation & Setup

```bash
git clone https://github.com/yourname/x-ai-agent
cd x-ai-agent
npm install
```

Set up your `.env` file:

```env
GEMINI_API_KEY=your_gemini_api_key
PORT=3000
```

Run the development server:

```bash
npm run dev
```

---

## 🧩 Adding New Tools

Create a new file in `tools/yourtool.js`:

```js
module.exports = {
  name: "yourtool",
  description: "Describe what your tool does",
  inputSchema: { type: "object", properties: {} },
  run: async (input) => {
    // Your logic here
    return { result: "Tool output" };
  }
};
```

The MCP server will automatically register and expose it to the agent.

---

## 🌍 Use Cases

* AI developer assistants
* Automated research agents
* Workflow/task automation
* Voice/chat-based intelligent interfaces
* Context-aware multi-agent systems

---

## 🤝 Contributing

Pull requests and ideas are welcome! If you find a bug or want to add a feature, feel free to open an issue or submit a PR.

---

## 📄 License

MIT License — use, modify, and share freely.

---

## ⭐️ Show Your Support

If you find this project helpful, consider giving it a star 🌟 to support development!

---

Built with 💙 using Gemini 2.0 Flash and the Model Context Protocol.
