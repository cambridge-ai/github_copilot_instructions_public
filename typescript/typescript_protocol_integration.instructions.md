# TypeScript Protocol Integration Guide

This guide explains how to use TypeScript instruction files in conjunction with the protocol specifications for comprehensive agent assistance.

## Core Identity & Activation

**ACTIVATION:** When integrating TypeScript development with specific protocols (REST, GraphQL, MCP, A2A), or combining multiple instruction files for comprehensive assistance, this instruction file becomes your primary guidance system.

**EXPERTISE SCOPE:** TypeScript protocol integration, multi-domain instruction coordination, protocol-specific TypeScript implementations, and comprehensive development guidance across different domains.

## Combining Instructions

When working on TypeScript projects that implement specific protocols, combine relevant instruction files to create a comprehensive development guide:

1. **Start with Core Understanding**: Begin with the `typescript_guide.instructions.md` for fundamental TypeScript concepts.

2. **Add Domain-Specific Knowledge**: Include the relevant domain-specific file based on your project type:
   - Frontend web apps: `typescript_web_frontend.instructions.md`
   - Backend services: `typescript_backend.instructions.md`
   - API development: `typescript_api_development.instructions.md`
   - Full-stack applications: `typescript_full_stack.instructions.md`

3. **Include Protocol Instructions**: Add the relevant protocol file based on the API architecture:
   - REST APIs: `../protocols/rest_api.instructions.md`
   - Agent-to-Agent communication: `../protocols/a2a.instructions.md`
   - Model Context Protocol: `../protocols/mcp.instructions.md`

4. **Add Quality Practices**: Include `typescript_testing_quality.instructions.md` for comprehensive testing and quality assurance.

5. **Incorporate Best Practices**: Add `typescript_best_practices.instructions.md` for specific TypeScript optimizations and patterns.

## Example Combinations

### TypeScript MCP Server Development
```
typescript_guide.instructions.md
typescript_backend.instructions.md
typescript_api_development.instructions.md
../protocols/mcp.instructions.md
typescript_testing_quality.instructions.md
typescript_best_practices.instructions.md
```

### TypeScript REST API Client
```
typescript_guide.instructions.md
typescript_web_frontend.instructions.md
../protocols/rest_api.instructions.md
typescript_testing_quality.instructions.md
typescript_best_practices.instructions.md
```

### TypeScript A2A Agent Implementation
```
typescript_guide.instructions.md
typescript_full_stack.instructions.md
../protocols/a2a.instructions.md
typescript_testing_quality.instructions.md
typescript_best_practices.instructions.md
```

## Utility Integration

For project management and meta considerations, incorporate utility files:

1. **Project Management**: Include `../utils/project_management.instructions.md` for tasks, planning, and organization.

2. **Meta-Prompting**: Add `../utils/metaprompting.instructions.md` for instruction refinement and agent optimization.

## Prioritization Order

When multiple instruction files might have conflicting guidance, prioritize in this order:

1. Protocol-specific requirements (from protocol files)
2. TypeScript domain-specific practices (from domain files)
3. General TypeScript best practices (from best practices file)
4. Project management considerations (from utilities)

This ensures that protocol compliance is maintained while leveraging idiomatic TypeScript patterns and best practices.
