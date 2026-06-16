# What is MCP?  

Model Context Protocol (MCP) is an open-source standard developed by Anthropic facilitate the connection between AI applications and external data sources, tools, and systems. 

MCP Server:  

MCP Client: 

Host:  

## MCP vs RAG 

In RAG, the developer is often responsible for compiling and maintaining the external database. With MCP, the developer of the MCP server (usually the same party that owns the external data source) controls and maintains that data. Developers can simply connect to the MCP server  

Owners of the data source, tool, etc., can now share on their terms. This also limits redundancy.   

Example: building a chatbot for compiling and recommending latest research in Computer Science. Using RAG, the. Developer will have to compile that database of papers, often by scraping content from a publisher like Wiley or a database like Scopus. They are additionally responsible for storing, updating, and maintaining that database. Add to how it limits redundancy.  

Both RAG and MCP help with language models’ currency of knowledge.   

MCP goes beyond RAG to offer dynamic and live access.  

 

Improves accuracy and transparency. And attribution.  

# Getting Started with MCP

The [official MCP GitHub organization](https://github.com/modelcontextprotocol) is maintained by Anthropic and is the home of the protocol specification, SDKs, and [reference implementations of MCP servers](https://github.com/modelcontextprotocol/servers).  

The official MCP Registry can be found at [registry.modelcontextprotocol.io/](https://registry.modelcontextprotocol.io/). Not that this is community-contributed includes details of their authentication methods. 

Other such directories can be found online, such as:  

- https://mcpservers.org/ 
- https://mcpmarket.com/ 

 

As with any open-source project, community-contributed MCP servers vary in quality and maintenance. Because MCP servers can act on your behalf by reading files, making requests, and accessing data, it is good practice to check who maintains the servers and what access/permissions it requires before connecting a server to institutional systems or sensitive data. Potential indicators of activity and community trust include the number of GitHub stars and commit history.  

## Tutorials 
Tutorials 

- [MCP: Build Rich-Context AI Apps with Anthropic](https://www.deeplearning.ai/short-courses/mcp-build-rich-context-ai-apps-with-anthropic/) 