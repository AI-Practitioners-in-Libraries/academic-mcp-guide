# Academic MCP Guide and Directory
A curated directory of MCP servers relevant to academic libraries, research, and higher education. Maintained by the AI Practitioners in Libraries Community of Practice. 

Interested in contributing? See [CONTRIBUTING.md](CONTRIBUTING.md).

## Table of Contents

- [What is MCP?](#what-is-mcp)
- [MCP vs RAG](#mcp-vs-rag)
- [Getting Started](#getting-started-with-mcp)
- [Academic MCP Server Directory](#academic-mcp-servers)
- [How to Evaluate Servers](#how-to-evaluate-servers)

## What is MCP?  

Model Context Protocol (MCP) is an open-source standard developed by Anthropic that facilitates the connection between AI applications and external data sources, tools, and systems. 

### Why MCP Matters
Before MCP, connecting an AI application to external data sources required custom, unique integrations. Each tool, database, or service would need its own connector, which would have to be built and maintained separately. MCP replaces that fragmented approach with a universal standard: once a system has an MCP server, any MCP-compatible application can connect to it directly. This dramatically lowers the engineering effort required on both sides. Developers, database providers, and publishers only need to implement the standard once (build an MCP server), and their tools, publications, and datasets will immediately be accessible to any AI application developer. For users, MCP facilitates access to a growing library of tools, data sources, and other services.  

### Key Terms 
**MCP Server**: a program that exposes data, tools, or capabilities to AI applications via the MCP standard. It acts as a bridge between the AI and an external system, such as a database or third-party service. It takes requests from MCP clients and returns relevant context or results. 

**MCP Client**: the component within an AI application that initiates communication with MCP servers. It sends requests for data or tool use and processes the responses returned by the server.  

**Host**: the AI application or environment in which the MCP client runs. Examples include Claude Desktop, an IDE plugin, or a custom AI assistant. The host manages the client's connections to MCP servers.  

### MCP vs RAG 

Another common approach to connecting AI with external information is Retrieval-Augmented Generation, or RAG. Both RAG and MCP helps maintain knowledge currency and allow AI applications or models to draw on outside sources rather than relying solely on what the model learned during training. They differ in how that outside information is managed. 

With RAG, the developer building the application is often responsible for compiling and maintaining the external database. For example, a developer building a chatbot to recommend the latest Computer Science research might have to scrape papers from publishers like Wiley or databases like Scopus, then store, update, and maintain that collection on their own.  

Because MCP servers are typically built and maintained by the owners of the data source, developers and users can simply connect to an existing server. This reduces redundancy: instead of having each developer scrape and storing copies of the same content, everyone can simply connect to the same server. A publisher like Wiley can maintain their own MCP server and give AI applications direct, live access to their catalog on their own terms, including any licensing or access restrictions they want to enforce. 

MCP goes beyond RAG to offer dynamic, real-time access to data, whereas RAG typically relies on a snapshot of information that must be updated. This makes MCP well-suited for applications where information currency matters. 
 
## Getting Started with MCP

### Tutorials  

- [MCP: Build Rich-Context AI Apps with Anthropic](https://www.deeplearning.ai/short-courses/mcp-build-rich-context-ai-apps-with-anthropic/) 

The [official MCP GitHub organization](https://github.com/modelcontextprotocol) is maintained by Anthropic and is the home of the protocol specification, SDKs, and [reference implementations of MCP servers](https://github.com/modelcontextprotocol/servers).  

### Registries and Directories

The official MCP Registry can be found at [registry.modelcontextprotocol.io/](https://registry.modelcontextprotocol.io/). Note that this is community-contributed includes details of their authentication methods. 

Other such directories can be found online, such as:  

- https://mcpservers.org/ 
- https://mcpmarket.com/ 

## Academic MCP Servers

| Server | Data Source | Developer | Access |
|--------|-------------|-----------|--------|
| [Wiley Scholar Gateway (pilot version)](https://www.wiley.com/en-us/research/scholar-gateway-connect-claude-mistral-ai/) | Subset of the Wiley portfolio, excluding content published after September 2025 | Wiley | Free Trial | 
| [Elsevier Scopus](https://github.com/qwe4559999/scopus-mcp) | Elsevier Scopus API | Community | Institutional/API key | 
| [ArXiv](https://github.com/blazickjp/arxiv-mcp-server) | ArXiv's repository | Community | Free | 
| [Google Scholar](https://github.com/JackKuo666/Google-Scholar-MCP-Server) | Google Scholar papers | Community | Free |

### How to Evaluate Servers

As with any open-source project, community-contributed MCP servers vary in quality and maintenance. Because MCP servers can act on your behalf by reading files, making requests to external sources, and accessing data, users should carefully evaluate any server before connecting it to institutional systems or sensitive data. It is considered good practice to check who maintains the server and what permissions it requires before use. Indicators of an active, trustworthy server include the number of GitHub stars (a measure of community endorsement) and its commit history (a record of how recently and frequently the code has been updated). 