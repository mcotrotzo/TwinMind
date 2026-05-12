# TwinMind — A Modelling Copilot for Digital Twins

**TwinMind** is an AI-powered modelling copilot that bridges natural language and formal system modelling. It takes human-written descriptions of systems, components, or behaviours, understands their structure and semantics, and automatically generates SysML v1 models inside Enterprise Architect — no manual diagram-drawing required.

## How it works

The user provides a plain-text description of a system — for example, a microgrid, a cyber-physical device, or any other engineered system. TwinMind processes this input using a [LangChain](https://docs.langchain.com/oss/python/langchain/agents) agent pipeline that interprets the described entities, relationships, and properties. The agent then interacts with Enterprise Architect via a dedicated MCP server, programmatically constructing a structured SysML model from the extracted information.

All generated models conform to the **UIBK SysML v1 Digital Twin Library** ([`cloud-DTs/SysML2CMAdapter`](https://github.com/cloud-DTs/SysML2CMAdapter)), ensuring that the output is consistent with the established Digital Twin profile used at the University of Innsbruck — including stereotypes, tagged values, and architectural conventions defined in that library.

## Key Components

| Component | Role |
|---|---|
| **Natural language understanding** | LangChain agents parse and decompose the user's input into modelling-relevant concepts |
| **Enterprise Architect integration** | An EA MCP server exposes the EA automation API, allowing the agent to create packages, blocks, ports, connectors, and stereotypes programmatically |
| **UIBK Digital Twin profile** | Generated models are grounded in the SysML v1 Digital Twin Library, guaranteeing structural validity and reusability within the broader UIBK toolchain |
## Useful Technologies
* Cherry Studio. With this the tool can ue multiple LLM models
* Langchain
* MCP EA https://www.sparxsystems.jp/en/MCP/

