# GitHub Copilot Instructions

A collection of GitHub Copilot Agent instructions grouped by technology to enhance your coding experience with up-to-date knowledge across all technology domains.

## 📚 Complete Documentation

For comprehensive documentation, see the [`/docs`](docs/) directory:

- **[Getting Started](docs/getting-started.md)** - Installation, setup, and first project
- **[User Guide](docs/user-guide.md)** - Effective usage patterns and combinations  
- **[Examples](docs/examples/)** - Real-world scenarios and project templates
- **[Reference](docs/reference/)** - Complete instruction catalog and API reference
- **[Troubleshooting](docs/troubleshooting.md)** - Common issues and solutions
- **[Development Guide](docs/development-guide.md)** - Contributing new instructions
- **[Architecture](docs/architecture.md)** - Repository structure and design principles

## Quick Start

1. **Clone the repository**:
   ```bash
   git clone https://github.com/cambridge-ai/github_copilot_instructions_public.git
   ```

2. **Configure VS Code**:
   - Open Settings (`Cmd+,` or `Ctrl+,`)
   - Search for "Instructions"
   - Add to "Chat: Instructions Files Locations":
     ```
     /path/to/github_copilot_instructions_public/public/**/*.instructions.md
     ```

3. **Start developing**: GitHub Copilot will now follow the instruction protocols!

## Overview

This repository contains custom instruction files for GitHub Copilot to help optimize AI assistance for different technologies and use cases. These instructions help Copilot provide more contextually appropriate and useful code suggestions based on the specific technology you're working with, while ensuring the agent stays current with the latest technologies, frameworks, libraries, and best practices across ALL domains.

## Core Features

All instruction files include:

- **🔄 Web Search Capabilities**: Instructions for implementing web search to check for the latest technologies
- **🧠 Comprehensive Knowledge**: Guidance for maintaining current knowledge across ALL domains  
- **📈 Continuous Updates**: Processes for keeping up with new releases, versions, and best practices
- **🌐 Cross-Domain Awareness**: Mechanisms to stay current with trends in every relevant technology sector
- **⚡ Core Development Protocol**: Disciplined development process with specs, testing, and quality gates

## Repository Structure

### 🏗️ Core Behaviours
- **[`core_dev.instructions.md`](public/core_behaviours/core_dev.instructions.md)**: Professional development protocol with approval gates, testing requirements, and documentation standards

### 🚀 All-in-One Solutions
Complete, opinionated stacks for rapid development:
- **[`nestjs_api_service.instructions.md`](public/aio/nestjs_api_service.instructions.md)**: Complete NestJS API service
- **[`python_api_service.instructions.md`](public/aio/python_api_service.instructions.md)**: Complete Python API service  
- **[`react_frontend_application.instructions.md`](public/aio/react_frontend_application.instructions.md)**: Complete React frontend

### 🐍 Python Instructions
Comprehensive Python development guidance:
- **[`python_guide.instructions.md`](public/python/python_guide.instructions.md)**: Core Python language foundation
- **[`python_api_development.instructions.md`](public/python/python_api_development.instructions.md)**: REST API development
- **[`python_data_science.instructions.md`](public/python/python_data_science.instructions.md)**: Data science and ML
- **[`python_web_development.instructions.md`](public/python/python_web_development.instructions.md)**: Web applications
- **[`python_testing_quality.instructions.md`](public/python/python_testing_quality.instructions.md)**: Testing and QA

### 📘 TypeScript Instructions  
Complete TypeScript ecosystem coverage:
- **[`typescript_guide.instructions.md`](public/typescript/typescript_guide.instructions.md)**: Core TypeScript foundation
- **[`typescript_full_stack.instructions.md`](public/typescript/typescript_full_stack.instructions.md)**: Full-stack development
- **[`typescript_api_development.instructions.md`](public/typescript/typescript_api_development.instructions.md)**: Backend APIs
- **[`typescript_web_frontend.instructions.md`](public/typescript/typescript_web_frontend.instructions.md)**: Frontend development
- **[`typescript_testing_quality.instructions.md`](public/typescript/typescript_testing_quality.instructions.md)**: Testing and QA

### 🔗 Protocol Instructions
Communication and integration patterns:
- **[`rest_api.instructions.md`](public/protocols/rest_api.instructions.md)**: REST API development standards
- **[`mcp.instructions.md`](public/protocols/mcp.instructions.md)**: Model Context Protocol implementation
- **[`a2a.instructions.md`](public/protocols/a2a.instructions.md)**: Agent-to-Agent communication
- **[`agent.instructions.md`](public/protocols/agent.instructions.md)**: AI Agent development

### 🛠️ Utilities
Meta-development and project management:
- **[`project_management.instructions.md`](public/utils/project_management.instructions.md)**: Project workflow optimization
- **[`metaprompting.instructions.md`](public/utils/metaprompting.instructions.md)**: AI interaction optimization
- **[`agent_creation.instructions.md`](public/utils/agent_creation.instructions.md)**: AI agent development

## Recommended Combinations

### 🎯 Production API Development
```
core_dev.instructions.md (automatic)
python_guide.instructions.md
python_api_development.instructions.md  
rest_api.instructions.md
python_testing_quality.instructions.md
```

### ⚡ Rapid Prototyping
```
core_dev.instructions.md (automatic)
python_api_service.instructions.md (All-in-One)
```

### 🌐 Full-Stack Web Application
```
core_dev.instructions.md (automatic)
typescript_guide.instructions.md
typescript_full_stack.instructions.md
typescript_testing_quality.instructions.md
```

### 🤖 AI Agent Development
```
core_dev.instructions.md (automatic)
python_guide.instructions.md
agent.instructions.md
mcp.instructions.md
python_testing_quality.instructions.md
```

For more combinations and detailed guidance, see the [User Guide](docs/user-guide.md).

## How to Use

### VS Code Setup
1. **Open Settings**: `Cmd+,` (Mac) or `Ctrl+,` (Windows/Linux)
2. **Search**: Type "Instructions" in the search bar  
3. **Configure**: Find "Chat: Instructions Files Locations" and add:
   ```
   /path/to/github_copilot_instructions_public/public/**/*.instructions.md
   ```
4. **Restart**: VS Code to load the instructions

### Core Development Workflow
When you start any project, GitHub Copilot will automatically:
1. **📋 Create Specifications**: Establish `.github/SPECS.md` with your approval
2. **📝 Manage Tasks**: Maintain `.github/TODO.md` as a rolling task list
3. **🔍 Enforce Quality**: Apply modularity, testing, and approval gates
4. **📚 Maintain Docs**: Keep comprehensive documentation in `/docs`

For detailed setup and usage instructions, see the [Getting Started Guide](docs/getting-started.md).

## Technology Currency

Each instruction file includes specific guidance for maintaining up-to-date knowledge:
- **🐍 Python**: Monitors PyPI, GitHub, and community forums for new releases and trends
- **📘 TypeScript**: Tracks npm, GitHub, and community resources for latest frameworks  
- **🔗 Protocols**: Stay current with latest specifications and implementations
- **🤖 AI Agents**: Comprehensive web searching across ALL technology domains

## Contributing

We welcome contributions! Please see our [Development Guide](docs/development-guide.md) for:
- Contributing new instruction files
- Improving existing instructions  
- Testing and validation procedures
- Code review process

## License

This project is licensed under the terms included in the [LICENSE](LICENSE) file.
