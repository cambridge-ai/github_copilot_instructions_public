# Getting Started Guide

## Quick Setup

### 1. Clone the Repository
```bash
git clone https://github.com/cambridge-ai/github_copilot_instructions_public.git
cd github_copilot_instructions_public
```

### 2. Configure VS Code
1. Open VS Code Settings (`Cmd+,` on Mac, `Ctrl+,` on Windows/Linux)
2. Search for "Instructions"
3. Find "Chat: Instructions Files Locations"
4. Add the repository path:
   ```
   /path/to/github_copilot_instructions_public/public/**/*.instructions.md
   ```

### 3. Verify Installation
- Open any project in VS Code
- Start a GitHub Copilot chat
- The AI should now follow the instruction protocols

## Configuration Options

### Option 1: All Instructions (Recommended for New Users)
```
/path/to/github_copilot_instructions_public/public/**/*.instructions.md
```
**Pros**: Complete coverage, all features available
**Cons**: May be overwhelming for simple projects

### Option 2: Selective Configuration
Add specific instruction files based on your needs:
```
/path/to/github_copilot_instructions_public/public/core_behaviours/core_dev.instructions.md
/path/to/github_copilot_instructions_public/public/python/python_guide.instructions.md
/path/to/github_copilot_instructions_public/public/python/python_api_development.instructions.md
```

### Option 3: AIO Configuration
For rapid development with opinionated setups:
```
/path/to/github_copilot_instructions_public/public/core_behaviours/core_dev.instructions.md
/path/to/github_copilot_instructions_public/public/aio/python_api_service.instructions.md
```

## First Project Setup

### Following Core Development Protocol

1. **Create Project Specifications**
   ```bash
   mkdir .github
   touch .github/SPECS.md
   ```

2. **Define Project Requirements**
   Edit `.github/SPECS.md` with your project specifications:
   ```markdown
   # Project Specifications
   
   ## Overview
   [Project description]
   
   ## Technical Requirements
   - Language: Python/TypeScript
   - Framework: [Framework choice]
   - Testing: [Testing requirements]
   
   ## Architecture
   [System architecture description]
   ```

3. **Initialize Task Management**
   ```bash
   touch .github/TODO.md
   ```

4. **Set Up Documentation**
   ```bash
   mkdir docs
   touch docs/README.md
   ```

### Example: Python API Project

1. **Configure Instructions**
   Add these instruction files:
   - `core_dev.instructions.md` (automatic)
   - `python_guide.instructions.md`
   - `python_api_development.instructions.md`
   - `rest_api.instructions.md`
   - `python_testing_quality.instructions.md`

2. **Create Project Structure**
   ```bash
   mkdir src tests docs
   touch src/__init__.py
   touch tests/__init__.py
   touch requirements.txt
   touch pytest.ini
   ```

3. **Start Development**
   - Begin with GitHub Copilot chat
   - AI will follow the specified protocols
   - Maintain SPECS.md and TODO.md as you progress

## Validation Checklist

After setup, verify these items work correctly:

- [ ] GitHub Copilot recognizes the instruction files
- [ ] AI asks for SPECS.md agreement before starting development
- [ ] AI maintains TODO.md with task updates
- [ ] AI suggests modular code patterns
- [ ] AI recommends appropriate testing strategies
- [ ] AI requests approval for major changes (≥50 lines)
- [ ] AI maintains documentation in /docs

## Common Setup Issues

### Instructions Not Loading
- **Issue**: AI doesn't follow the protocols
- **Solution**: Check VS Code settings path is correct and files exist
- **Debug**: Restart VS Code after configuration changes

### Path Resolution Problems
- **Issue**: Glob patterns not working
- **Solution**: Use absolute paths instead of relative paths
- **Alternative**: Copy instruction files to a known location

### Multiple Instruction Conflicts
- **Issue**: Contradictory guidance from different files
- **Solution**: Review [architecture documentation](architecture.md) for precedence rules
- **Fix**: Use more specific instruction combinations

## Next Steps

1. Review the [User Guide](user-guide.md) for effective usage patterns
2. Explore [Examples](examples/) for real-world scenarios
3. Check [Development Guide](development-guide.md) if you want to contribute
4. Reference [Troubleshooting](troubleshooting.md) for common issues
