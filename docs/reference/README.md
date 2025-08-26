# Instruction File Reference

## Complete Catalog

### Core Behaviours
| File | Purpose | Required | Dependencies |
|------|---------|----------|--------------|
| `core_dev.instructions.md` | Development protocol and standards | ✅ Always | None |

### Language Foundations
| File | Purpose | Technology | Dependencies |
|------|---------|------------|--------------|
| `python_guide.instructions.md` | Python language foundation | Python | core_dev |
| `typescript_guide.instructions.md` | TypeScript language foundation | TypeScript/JavaScript | core_dev |

### Python Specializations
| File | Purpose | Use Case | Dependencies |
|------|---------|----------|--------------|
| `python_api_development.instructions.md` | REST API development | Web APIs | python_guide |
| `python_data_science.instructions.md` | Data analysis and ML | Data Science | python_guide |
| `python_web_development.instructions.md` | Web applications | Web Apps | python_guide |
| `python_scripting.instructions.md` | Automation and scripting | DevOps/Automation | python_guide |
| `python_testing_quality.instructions.md` | Testing and quality assurance | All Python projects | python_guide |
| `python_best_practices.instructions.md` | Advanced Python patterns | Advanced Python | python_guide |

### TypeScript Specializations
| File | Purpose | Use Case | Dependencies |
|------|---------|----------|--------------|
| `typescript_api_development.instructions.md` | API development | Backend APIs | typescript_guide |
| `typescript_backend.instructions.md` | Server-side development | Backend Services | typescript_guide |
| `typescript_web_frontend.instructions.md` | Frontend development | Web UIs | typescript_guide |
| `typescript_full_stack.instructions.md` | Complete web applications | Full-stack Apps | typescript_guide |
| `typescript_testing_quality.instructions.md` | Testing and QA | All TS projects | typescript_guide |
| `typescript_best_practices.instructions.md` | Advanced TypeScript | Advanced TS | typescript_guide |
| `typescript_protocol_integration.instructions.md` | Protocol integration guide | Complex integrations | typescript_guide |

### Communication Protocols
| File | Purpose | Protocol | Dependencies |
|------|---------|----------|--------------|
| `rest_api.instructions.md` | REST API patterns | HTTP/REST | Language guide |
| `mcp.instructions.md` | Model Context Protocol | MCP | Language guide |
| `a2a.instructions.md` | Agent-to-Agent communication | Agent Systems | Language guide |
| `agent.instructions.md` | AI Agent development | AI Agents | Language guide |

### All-in-One Solutions
| File | Purpose | Stack | Dependencies |
|------|---------|--------|--------------|
| `nestjs_api_service.instructions.md` | Complete NestJS API | NestJS + TypeScript | core_dev |
| `python_api_service.instructions.md` | Complete Python API | FastAPI + Python | core_dev |
| `react_frontend_application.instructions.md` | Complete React app | React + TypeScript | core_dev |

### Utilities
| File | Purpose | Domain | Dependencies |
|------|---------|--------|--------------|
| `project_management.instructions.md` | Project workflow | Management | core_dev |
| `metaprompting.instructions.md` | Prompt optimization | AI Interaction | None |
| `agent_creation.instructions.md` | Agent development | AI Development | None |

## Configuration Patterns

### Standard Combinations

#### Python Web API
```
core_dev.instructions.md (automatic)
python_guide.instructions.md
python_api_development.instructions.md
rest_api.instructions.md
python_testing_quality.instructions.md
```

#### TypeScript Full-Stack
```
core_dev.instructions.md (automatic)
typescript_guide.instructions.md
typescript_full_stack.instructions.md
typescript_web_frontend.instructions.md
typescript_testing_quality.instructions.md
```

#### Data Science Project
```
core_dev.instructions.md (automatic)
python_guide.instructions.md
python_data_science.instructions.md
python_testing_quality.instructions.md
```

#### AI Agent Development
```
core_dev.instructions.md (automatic)
python_guide.instructions.md (or typescript_guide.instructions.md)
agent.instructions.md
mcp.instructions.md (optional)
{language}_testing_quality.instructions.md
```

#### Rapid Prototyping
```
core_dev.instructions.md (automatic)
{technology}_api_service.instructions.md (AIO)
```

### Advanced Combinations

#### Microservices Architecture
```
Per Service:
- core_dev.instructions.md
- {language}_guide.instructions.md
- {language}_api_development.instructions.md
- rest_api.instructions.md
- a2a.instructions.md

Cross-Service:
- project_management.instructions.md
```

#### Agent Ecosystem
```
core_dev.instructions.md (automatic)
{language}_guide.instructions.md
agent.instructions.md
mcp.instructions.md
a2a.instructions.md
{language}_testing_quality.instructions.md
```

## Configuration Reference

### VS Code Settings
```json
{
  "chat.instructionsFilesLocations": [
    "/path/to/github_copilot_instructions_public/public/**/*.instructions.md"
  ]
}
```

### Selective Configuration
```json
{
  "chat.instructionsFilesLocations": [
    "/path/to/github_copilot_instructions_public/public/core_behaviours/core_dev.instructions.md",
    "/path/to/github_copilot_instructions_public/public/python/python_guide.instructions.md",
    "/path/to/github_copilot_instructions_public/public/python/python_api_development.instructions.md"
  ]
}
```

### Team Configuration Template
```json
{
  "chat.instructionsFilesLocations": [
    "/shared/copilot-instructions/core/**/*.instructions.md",
    "/shared/copilot-instructions/team/**/*.instructions.md",
    "/path/to/github_copilot_instructions_public/public/{technology}/**/*.instructions.md"
  ]
}
```

## API Reference

### Core Protocol Functions

#### Project Initialization
- `establishSpecs()`: Create and validate .github/SPECS.md
- `initializeTasks()`: Set up .github/TODO.md
- `setupDocumentation()`: Create /docs structure

#### Development Workflow
- `validateModularity()`: Check code modularity standards
- `runTests()`: Execute appropriate test levels
- `requestApproval()`: Handle approval gates for major changes
- `updateDocumentation()`: Maintain comprehensive docs

#### Quality Gates
- `checkLineThreshold()`: Validate 50+ line approval requirement
- `validateTests()`: Ensure test coverage standards
- `verifyDocumentation()`: Check documentation completeness

### Instruction File Hooks

#### Language Integration
- `setLanguageFoundation()`: Establish language-specific base
- `applyDomainSpecializations()`: Add domain-specific patterns
- `integrateProtocols()`: Include communication protocols

#### Quality Integration
- `applyTestingStandards()`: Include testing requirements
- `enforceCodeQuality()`: Apply linting and formatting
- `validateSecurity()`: Include security checks

### Extension Points

#### Custom Instructions
- Directory: `user/` for custom instruction files
- Precedence: Override public instructions
- Integration: Automatic loading with public instructions

#### Team Standards
- Custom approval thresholds
- Specific coding standards
- Enhanced quality gates
- Team-specific protocols

## Troubleshooting Reference

### Common Issues

| Issue | Symptom | Solution | Reference |
|-------|---------|----------|-----------|
| Instructions not loading | AI doesn't follow protocols | Check VS Code settings path | [Getting Started](../getting-started.md) |
| Conflicting guidance | Inconsistent AI behavior | Review instruction precedence | [Architecture](../architecture.md) |
| Missing approvals | No approval requests | Verify core_dev.instructions.md loaded | [User Guide](../user-guide.md) |
| Test failures | Quality gates failing | Check testing instruction integration | [Development Guide](../development-guide.md) |

### Debug Commands

#### Verify Configuration
```bash
# Check VS Code settings
code --list-extensions | grep copilot
cat ~/.vscode/settings.json | grep instructions

# Validate instruction files
find /path/to/instructions -name "*.instructions.md" -exec echo {} \;
```

#### Test Instruction Loading
```bash
# Test with simple project
mkdir test-project && cd test-project
echo "Test GitHub Copilot instruction loading" > README.md
# Open in VS Code and test Copilot chat
```

### Performance Optimization

#### Selective Loading
- Use specific instruction files instead of glob patterns
- Avoid loading conflicting instruction sets
- Regular cleanup of unused instructions

#### Memory Management
- Monitor VS Code memory usage with many instructions
- Consider instruction file size and complexity
- Use AIO instructions for simpler configurations
