# GitHub Copilot Instructions

A collection of GitHub Copilot Agent instructions grouped by technology to enhance your coding experience with up-to-date knowledge across all technology domains.

## Overview

This repository contains custom instruction files for GitHub Copilot to help optimize AI assistance for different technologies and use cases. These instructions help Copilot provide more contextually appropriate and useful code suggestions based on the specific technology you're working with, while ensuring the agent stays current with the latest technologies, frameworks, libraries, and best practices across ALL domains.

## Key Features

All instruction files include:

- **Web Search Capabilities**: Instructions for implementing web search to check for the latest technologies
- **Comprehensive Knowledge**: Guidance for maintaining current knowledge across ALL domains
- **Continuous Updates**: Processes for keeping up with new releases, versions, and best practices
- **Cross-Domain Awareness**: Mechanisms to stay current with trends in every relevant technology sector

## Repository Structure

- **protocols/**: Instructions for various communication protocols
  - `a2a.instructions.md`: Agent-to-Agent communication instructions
  - `mcp.instructions.md`: Model Context Protocol instructions
  - `rest_api.instructions.md`: REST API development instructions
  - `agent.instructions.md`: AI Agent development instructions

- **python/**: Instructions for Python development
  - `python_api_development.instructions.md`: Python API development best practices
  - `python_best_practices.instructions.md`: General Python best practices
  - `python_data_science.instructions.md`: Data science with Python
  - `python_guide.instructions.md`: General Python guidance
  - `python_scripting.instructions.md`: Python scripting instructions
  - `python_testing_quality.instructions.md`: Python testing and quality assurance
  - `python_web_development.instructions.md`: Python web development
  
- **typescript/**: Instructions for TypeScript development
  - `typescript_guide.instructions.md`: General TypeScript guidance
  - `typescript_api_development.instructions.md`: TypeScript API development best practices
  - `typescript_backend.instructions.md`: TypeScript backend development
  - `typescript_web_frontend.instructions.md`: TypeScript web frontend development
  - `typescript_full_stack.instructions.md`: TypeScript full-stack development
  - `typescript_testing_quality.instructions.md`: TypeScript testing and quality assurance
  - `typescript_best_practices.instructions.md`: TypeScript best practices
  - `typescript_protocol_integration.instructions.md`: Guide for integrating TypeScript with protocols
  
- **utils/**: Utility instructions for project management and meta-prompting
  - `project_management.instructions.md`: Project management guidance
  - `metaprompting.instructions.md`: Instructions for refining and optimizing prompts

## Combining Instructions

These instruction files are designed to be used together for comprehensive assistance:

1. **Base Language Instructions**: Start with the general guide for your language (`python_guide.instructions.md` or `typescript_guide.instructions.md`)
2. **Domain-Specific Instructions**: Add instructions specific to your project type (API, web, data science, etc.)
3. **Protocol Instructions**: Include relevant protocol files when implementing specific communication patterns
4. **Quality Assurance**: Add testing and quality instruction files for comprehensive testing guidance
5. **Utilities**: Include utility instructions for project management or prompt optimization

See `typescript_protocol_integration.instructions.md` for examples of combining instruction files for specific project types.

## Technology Currency

Each instruction file includes specific guidance for maintaining up-to-date knowledge:

- **Python Guide**: Monitors PyPI, GitHub, and community forums for new releases and trends
- **TypeScript Guide**: Tracks npm, GitHub, and community resources for latest frameworks and libraries
- **Protocol Files**: Stay current with latest specifications and implementations
- **Agent Instructions**: Implement comprehensive web searching across ALL domains

By using these instruction files, GitHub Copilot will help you stay current with the latest developments in your technology stack and provide recommendations based on the most up-to-date best practices.

## How to Use These Instructions in VS Code

To add these custom instructions to GitHub Copilot in Visual Studio Code:

1. Open VS Code Settings
   - Press `Cmd+,` (Mac) or `Ctrl+,` (Windows/Linux)
   - Or go to Code > Preferences > Settings

2. Search for "Instructions"
   - Type "Instructions" in the search bar

3. Find "Chat: Instructions Files Locations"
   - Look for the setting labeled "Chat: Instructions Files Locations"

4. Add File Paths
   - Click "Add Item" and enter the absolute or relative path to the instruction files you want to use
   - You can add individual files or use glob patterns like:
     ```
     /Users/username/Documents/dev/github_copilot_instructions/**/*.instructions.md
     ```

5. Save the settings

Once configured, GitHub Copilot will use these instructions to provide more targeted assistance when working with the corresponding technologies.

## Contributing

Feel free to contribute by adding new instruction files for other technologies or improving existing ones by submitting pull requests.

## License

This project is licensed under the terms included in the [LICENSE](LICENSE) file.
