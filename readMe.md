# MCP 🚀
![MCP Tool Call Demo](/static/mcp-tool-call.gif)

## MCP (Model Context Protocol)

**What it's not:**
1. A framework for building agents
2. A fundamental change to how agents work
3. A way to code agents

**What it is:**
1. A protocol - a standard
2. A simple way to integrate tools, resoruces, prompts
3. "A USB-C port for AI applications"

**Reasons not to be excited**
1. It's just a standard, it's not tools themselves
2. LangChain already has big Tools ecosystem
3. You can already make any function into a Tool

**Reasone to be excited**
1. Makes it frictionless to integrate
2. It's taking off! Exploding ecosystem
3. HTML was just a standard, too.


### MCP Core Concepts
(The three components)
1. **Host** is an LLM app like Claude or our Agent architecture
2. **MCP Client** lives inside Host and connects 1:1 to MCP Server
3. **MCP Server** provides tools, context and prompts

Example:
- Fetch is an **MCP Server** that searches the web via a headless browser
- You can configure **Claude Desktop**(The host) to run an MCP CLient that then launches the Fetch **MCP Server** on your computer

**Notes:** 
1. MCP Servers most often run on your box. Connecting to Remote MCP servers are less commmon.
2. Two "Transport" mechanisms: 
    i. **Stdio** spawns and communicates via standard input/output
    ii. Other one is **SSE (Server Side Events)** uses HTTPS connections with streaming. (Server streams back the result to LLM). 
    
    iii. SSE will be useful when we use the Remote MCP Server
    iv. When working on local we can use either of **Stdio** or **SSE**

### Why Make an MCP Server
1. Allow others to incorporate tools and resources
2. Consistently incorporate all our MCP Servers
3. Understand the plumbing (nuts and bolts)

### Reasons **not** to make an MCP server
1. If it's only for us, then we could just make tools the @function_tool decorator can make any function into a tool. (If we use MCP it should be broader usage and sharing tool)

### References
1. https://modelcontextprotocol.io/introduction
2. https://docs.cursor.com/context/model-context-protocol
3. https://github.com/modelcontextprotocol/quickstart-resources


### Check out the trace
https://platform.openai.com/traces

### Now take a look at some MCP marketplaces

https://mcp.so

https://glama.ai/mcp

https://smithery.ai/

https://huggingface.co/blog/LLMhacker/top-11-essential-mcp-libraries

HuggingFace great community article:
https://huggingface.co/blog/Kseniase/mcp


The Model Context Protocol (MCP) helps connect AI-agentic applications powered by Large Language Models (LLMs) to external tools and data sources, enabling more capable and context-aware AI systems.


## How it Works 🤔

This repository uses a unique branch-based structure for learning:

1.  **Each `project/*` branch covers a specific MCP feature or concept.**
2.  **Within each branch, commits are ordered chronologically.** Follow the commits one by one to learn the topic step-by-step.

Simply check out the branch for the topic you want to learn and walk through the commits!

## Available Topics (Branches) 📚

Here are the topics currently available:

*   `project/sse`: Learn how to implement Server-Sent Events (SSE) with MCP.
*   `project/langchain-mcp-adapters`: Explore integrating MCP with LangChain adapters.
*   `project/docker-mcp`: Understand how to containerize your MCP applications using Docker.

*More topics might be added, so keep an eye out!*

## Prerequisites 🛠️

Before you start, make sure you have the following installed:

*   🐍 Python (version 3.10 or higher)
*   📦 `uv` (the fast Python package installer and resolver)
*   ✨ Cursor IDE
*   ☁️ Claude Desktop

## Getting Started ▶️

1.  **Clone the repository:**
    ```bash
    git clone <>
    cd mcp-crash-course
    ```
2.  **Choose a topic and check out the branch:**
    ```bash
    # Example for the SSE topic
    git checkout project/sse
    ```
3.  **Follow the commits:** Use `git log --oneline --reverse` to see the chronological list of commits for the branch. Then, use `git checkout <commit_hash>` or your Git client to step through the history and learn.

## Contributing 🤝

Contributions are welcome! If you'd like to add a new topic or improve an existing one:

1.  Fork the repository.
2.  Create a new branch for your feature following the naming convention: `project/your-mcp-feature-name`.
3.  Make your changes, ensuring each commit represents a logical step in the learning process.
4.  Open a Pull Request against the `main` branch.


