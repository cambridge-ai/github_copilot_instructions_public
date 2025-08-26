# Architecture Overview

## Repository Structure

```
github_copilot_instructions_public/
├── docs/                          # Comprehensive documentation
├── public/                        # Public instruction files
│   ├── aio/                      # All-in-one instruction files
│   ├── core_behaviours/          # Core development protocols
│   ├── protocols/                # Communication protocol instructions
│   ├── python/                   # Python-specific instructions
│   ├── typescript/               # TypeScript-specific instructions
│   └── utils/                    # Utility and meta instructions
├── user/                         # User-specific customizations
├── .github/                      # Project governance (when following core protocol)
│   ├── SPECS.md                 # Project specifications
│   └── TODO.md                  # Rolling task management
└── README.md                    # High-level overview
```

## Instruction File Categories

### 1. Core Behaviours
- **Purpose**: Define fundamental development protocols and standards
- **Files**: `core_dev.instructions.md`
- **Usage**: Applied automatically to all projects following the development protocol

### 2. Language-Specific Instructions
- **Purpose**: Technology-specific guidance and best practices
- **Categories**:
  - Python: API development, data science, web development, testing
  - TypeScript: Frontend, backend, full-stack, API development
- **Usage**: Selected based on project technology stack

### 3. Protocol Instructions
- **Purpose**: Communication and integration patterns
- **Categories**:
  - Agent-to-Agent (A2A)
  - Model Context Protocol (MCP)
  - REST API
  - AI Agent development
- **Usage**: Applied when implementing specific communication patterns

### 4. All-in-One (AIO) Instructions
- **Purpose**: Comprehensive, opinionated setups for complete application stacks
- **Categories**:
  - NestJS API Service
  - Python API Service
  - React Frontend Application
- **Usage**: For rapid prototyping and standardized application development

### 5. Utility Instructions
- **Purpose**: Meta-development and project management
- **Categories**:
  - Agent creation
  - Project management
  - Meta-prompting
- **Usage**: Enhance development workflow and AI interaction

## Instruction File Design Principles

### 1. Modularity
- Each instruction file serves a specific purpose
- Files can be combined for comprehensive coverage
- No circular dependencies between instruction files

### 2. Technology Currency
- All files include web search capabilities
- Mechanisms for staying current with latest versions
- Community trend monitoring and adaptation

### 3. Actionable Guidance
- Clear, enforceable directives
- Specific implementation patterns
- Measurable quality criteria

### 4. Hierarchical Application
```
Base Language → Domain Specific → Protocols → Quality Assurance → Utilities
```

## Integration Patterns

### Standard Combination
```
1. Core Development Protocol (automatic)
2. Language Guide (python_guide.md OR typescript_guide.md)
3. Domain Instructions (api_development.md, web_development.md, etc.)
4. Protocol Instructions (if applicable)
5. Quality Instructions (testing_quality.md)
6. Utility Instructions (project_management.md)
```

### AIO Pattern
```
1. Core Development Protocol (automatic)
2. Single AIO file (e.g., nestjs_api_service.instructions.md)
3. Additional utilities as needed
```

## File Naming Convention

- **Language prefix**: `python_`, `typescript_`
- **Domain suffix**: `_api_development`, `_web_development`, `_testing_quality`
- **Extension**: `.instructions.md`
- **Special cases**: 
  - Core: `core_dev.instructions.md`
  - AIO: `{technology}_api_service.instructions.md`
  - Protocols: `{protocol}.instructions.md`

## Dependency Management

### Hard Dependencies
- All instruction files depend on core development protocol
- Language-specific files require corresponding guide file

### Soft Dependencies
- Quality files enhance any language-specific files
- Protocol files complement domain-specific implementations
- Utility files provide meta-enhancement

### Conflict Resolution
- More specific instructions override general ones
- Later-loaded files take precedence
- Core protocol cannot be overridden
