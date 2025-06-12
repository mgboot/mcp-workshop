# MCP Workshop

Welcome to the **Model Context Protocol (MCP) Workshop**! This repo provides a hands-on walkthrough for building and connecting an MCP client and server using Python, with optional Azure OpenAI integration.

---

## 🧩 Prerequisites

Before getting started, ensure you have the following installed:

- Python 3.9+
- [Node.js & npm](https://nodejs.org/) (required for MCP development tools)
- [Uvicorn](https://www.uvicorn.org/) (optional, for ASGI-based server testing)

---

## 📦 Installation

### 1. Install Python dependencies from `requirements.txt`:

```bash
pip install -r requirements.txt
```

### 2. Install Node.js, if not already installed:

- Download from [nodejs.org](https://nodejs.org/)

### 3. Set up Azure OpenAI credentials (optional but recommended for integration):

- Copy the `.env.sample` to `.env`:

```bash
cp .env.sample .env
```

- Fill in the following values:

```env
OPENAI_API_KEY=your-key-here
OPENAI_ENDPOINT=https://your-endpoint.openai.azure.com/
OPENAI_MODEL_NAME=gpt-4
OPENAI_DEPLOYMENT_NAME=your-deployment
```

---

## 📚 MCP SDK Setup

### 1. Install the official MCP SDK

Follow the instructions at:  
👉 https://github.com/modelcontextprotocol/python-sdk

### 2. Walk through the Quickstart tutorial

Found here:  
👉 https://modelcontextprotocol.info/docs/tutorials/quickstart/

This will help you build your own `server.py`.

---

## 🛠️ Create the MCP Server

Use the Quickstart to create `server.py`, then **add the following line to the end** of that file to make it executable as a standalone script:

```python
# Start the server
if __name__ == "__main__":
    mcp.run()
```

This enables `server.py` to be launched and communicate with clients via standard input/output.

---

## 🤖 Running the Client

With your server script ready, you're now set to connect with the client.

1. In PowerShell (e.g., VS Code terminal), run:

```bash
uv run client.py path\to\server.py
```

Example:

```bash
uv run client.py C:\Users\yourname\Documents\mcp-server-demo\server.py
```

2. If everything is set up properly, the client will launch in the console, connect to the MCP server, and allow you to submit queries that utilize the server’s tools and resources.

---

## ✅ Summary

You're now ready to:

- Use `client.py` to talk to a local MCP server
- Define and test new tools in `server.py`
- Integrate Azure OpenAI for LLM-powered functionality

---

## 📎 Resources

- [Model Context Protocol Docs](https://modelcontextprotocol.info/)
- [MCP Python SDK GitHub](https://github.com/modelcontextprotocol/python-sdk)
- [Azure OpenAI Quickstart](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/quickstart)
