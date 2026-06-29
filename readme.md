# Academic MCP Guide and Directory
A curated directory of MCP servers relevant to academic libraries, research, and higher education. Maintained by the AI Practitioners in Libraries Community of Practice. 

Potential use case: fork and further personalize to fit our specific institutions

# What is MCP?  

Model Context Protocol (MCP) is an open-source standard developed by Anthropic that facilitates the connection between AI applications and external data sources, tools, and systems. 

## Why MCP Matters
Before MCP, connecting an AI application to external data sources required custom, unique integrations. Each tool, database, or service would need its own connector, which would have to be built and maintained separately. MCP replaces that fragmented approach with a universal standard: once a system has an MCP server, any MCP-compatible application can connect to it directly. This has driven rapid adoption, because it dramatically lowers the engineering effort required on both sides. Developers, database providers, and publishers only need to implement the standard once (build an MCP server), and their tools, publications, and datasets will immediately be accessible to any AI application. For users, MCP facilitates access to a growing library of tools, data sources, and other services.  

## Key Terms 
**MCP Server**: a program that exposes data, tools, or capabilities to AI applications via the MCP standard. It acts as a bridge between the AI and an external system, such as a database or third-party service. It responds to requests from MCP clients and returns relevant context or results. 

**MCP Client** : the component within an AI application that initiates communication with MCP servers. It sends requests for data or tool use and processes the responses returned by the server.  

** Host** : the AI application or environment in which the MCP client runs. Examples include Claude Desktop, an IDE plugin, or a custom AI assistant. The host manages the client's connections to MCP servers.  

##MCP vs RAG 

Another common approach to connecting AI with external information is Retrieval-Augmented Generation, or RAG. Both RAG and MCP helps with LMs' currency of knowledge and allow AI applications or models to draw on outside sources rather than relying solely on what the model learned during training. They differ in how that outside information is managed. 

With RAG, the developer building the application is often responsible for compiling and maintaining the external database. For example, a developer building a chatbot to recommend the latest Computer Science research might have to scrape papers from publishers like Wiley or databases like Scopus, then store, update, and maintain that collection on their own.  

Because MCP servers are typically built and maintained by the owners of the data source, developers and users can simply connect to an existing server. A publisher like Wiley could maintain their own MCP server, giving AI applications direct, live access to their catalog on their own terms, including any licensing or access restrictions they want to enforce. This also reduces redundancy: instead of having each developer scrape and storing copies of the same content, everyone can simply connect to the same server.  

MCP goes beyond RAG to offer dynamic, real-time access to data, whereas RAG typically relies on a snapshot of information that must be updated. This makes MCP well-suited for applications where information currency matters. 
 
# Getting Started with MCP

The [official MCP GitHub organization](https://github.com/modelcontextprotocol) is maintained by Anthropic and is the home of the protocol specification, SDKs, and [reference implementations of MCP servers](https://github.com/modelcontextprotocol/servers).  

The official MCP Registry can be found at [registry.modelcontextprotocol.io/](https://registry.modelcontextprotocol.io/). Not that this is community-contributed includes details of their authentication methods. 

Other such directories can be found online, such as:  

- https://mcpservers.org/ 
- https://mcpmarket.com/ 

 

As with any open-source project, community-contributed MCP servers vary in quality and maintenance. Because MCP servers can act on your behalf by reading files, making requests to external sources, and accessing data, users should carefully evaluate any server before connecting it to institutional systems or sensitive data. It is considered good practice to check who maintains the server and what permissions it requires before use. Indicators of an active, trustworthy server include the number of GitHub stars (a measure of community endorsement) and its commit history (a record of how recently and frequently the code has been updated). 

## Tutorials 
Tutorials 

- [MCP: Build Rich-Context AI Apps with Anthropic](https://www.deeplearning.ai/short-courses/mcp-build-rich-context-ai-apps-with-anthropic/) 