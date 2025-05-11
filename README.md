# GitHub Copilot Instructions

A collection of GitHub Copilot Agent instructions grouped by technology to enhance your coding experience.

## Overview

This repository contains custom instruction files for GitHub Copilot to help optimize AI assistance for different technologies and use cases. These instructions help Copilot provide more contextually appropriate and useful code suggestions based on the specific technology you're working with.

## Repository Structure

- **protocols/**: Instructions for various communication protocols
  - `a2a.instructions.md`: Agent-to-Agent communication instructions
  - `mcp.instructions.md`: Model Context Protocol instructions
  - `rest_api.instructions.md`: REST API development instructions

- **python/**: Instructions for Python development
  - `python_api_development.instructions.md`: Python API development best practices
  - `python_best_practices.instructions.md`: General Python best practices
  - `python_data_science.instructions.md`: Data science with Python
  - `python_guide.instructions.md`: General Python guidance
  - `python_scripting.instructions.md`: Python scripting instructions
  - `python_testing_quality.instructions.md`: Python testing and quality assurance
  - `python_web_development.instructions.md`: Python web development

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
