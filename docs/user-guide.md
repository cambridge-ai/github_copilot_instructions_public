# User Guide

## Effective Usage Patterns

### Understanding Instruction Precedence

Instructions are applied in order of specificity:
1. **Core Protocol** (always active)
2. **Language Guide** (foundational)
3. **Domain Instructions** (specific use case)
4. **Protocol Instructions** (communication patterns)
5. **Quality Instructions** (testing and standards)
6. **Utility Instructions** (workflow enhancement)

### Choosing the Right Combination

#### For Web API Development
```
✅ Recommended Stack:
- core_dev.instructions.md (automatic)
- {language}_guide.instructions.md
- {language}_api_development.instructions.md
- rest_api.instructions.md
- {language}_testing_quality.instructions.md

🎯 Result: Disciplined API development with comprehensive testing
```

#### For Data Science Projects
```
✅ Recommended Stack:
- core_dev.instructions.md (automatic)
- python_guide.instructions.md
- python_data_science.instructions.md
- python_testing_quality.instructions.md

🎯 Result: Research-grade data analysis with reproducible results
```

#### For Full-Stack Applications
```
✅ Recommended Stack:
- core_dev.instructions.md (automatic)
- typescript_guide.instructions.md
- typescript_full_stack.instructions.md
- typescript_web_frontend.instructions.md
- typescript_testing_quality.instructions.md

🎯 Result: Production-ready full-stack application
```

#### For Rapid Prototyping
```
✅ Recommended Stack:
- core_dev.instructions.md (automatic)
- {technology}_api_service.instructions.md (AIO)

🎯 Result: Quick, opinionated setup with best practices
```

## Working with the Core Development Protocol

### Project Initialization Workflow

1. **Specification Phase**
   ```
   User: "I want to build a Python REST API for user management"
   AI: "Let's first establish the .github/SPECS.md. Please confirm these specifications..."
   ```

2. **Task Planning**
   ```
   AI Creates: .github/TODO.md
   - [ ] Set up project structure
   - [ ] Implement user model
   - [ ] Create authentication endpoints
   - [ ] Add input validation
   - [ ] Write comprehensive tests
   ```

3. **Iterative Development**
   ```
   Each Change:
   - AI implements feature
   - Updates TODO.md
   - Maintains documentation
   - Runs appropriate tests
   - Requests approval for major changes
   ```

### Managing Approval Gates

#### When AI Will Request Approval
- Changes ≥50 lines of code
- Architecture modifications
- Dependency additions
- Configuration changes

#### Approval Response Format
```
✅ Approved responses:
"Approved"
"Yes, proceed"
"Go ahead"
"Looks good"

❌ Rejection responses:
"No"
"Wait"
"Changes needed"
"Revise approach"
```

### Documentation Maintenance

#### Automatic Updates
The AI will maintain:
- `/docs/README.md` - Documentation index
- `/docs/api.md` - API documentation (for APIs)
- `/docs/architecture.md` - System architecture
- `/docs/setup.md` - Installation and setup
- `README.md` - High-level project overview

#### Manual Oversight
You should review:
- Technical accuracy of generated docs
- Business context and requirements
- User-facing documentation clarity

## Advanced Usage Patterns

### Custom Instruction Combinations

#### Agent Development
```
Instruction Stack:
- core_dev.instructions.md
- python_guide.instructions.md (or typescript_guide.instructions.md)
- agent.instructions.md
- mcp.instructions.md (if using Model Context Protocol)
- python_testing_quality.instructions.md
```

#### Multi-Service Architecture
```
Per Service:
- core_dev.instructions.md
- {language}_guide.instructions.md
- {language}_api_development.instructions.md
- a2a.instructions.md (for service communication)

Cross-Service:
- project_management.instructions.md
```

### Customization Strategies

#### Project-Specific Overrides
Create a `user/` directory with custom instructions:
```
user/
├── custom_standards.instructions.md
├── team_conventions.instructions.md
└── project_specific.instructions.md
```

#### Team Standards Integration
Modify core instructions to reflect team practices:
- Code review requirements
- Deployment procedures
- Security standards
- Performance benchmarks

## Quality Assurance Integration

### Test-Driven Development
```
AI Behavior with Testing Instructions:
1. Write test cases before implementation
2. Implement minimal code to pass tests
3. Refactor with test coverage validation
4. Update integration and e2e tests
```

### Code Quality Gates
```
Automatic Enforcement:
- Linting and formatting
- Type checking (TypeScript)
- Security scanning
- Performance benchmarks
- Documentation completeness
```

## Troubleshooting Common Patterns

### AI Not Following Protocol
**Symptoms**: No SPECS.md creation, missing TODO updates
**Solution**: Verify core_dev.instructions.md is loaded
**Check**: VS Code settings configuration

### Inconsistent Code Style
**Symptoms**: Mixed patterns, style violations
**Solution**: Ensure language guide is primary instruction
**Check**: Instruction precedence order

### Over-Engineering
**Symptoms**: Excessive abstraction, complex patterns
**Solution**: Emphasize simplicity in SPECS.md
**Check**: Review modularity requirements

### Under-Testing
**Symptoms**: Missing test coverage, integration gaps
**Solution**: Add testing quality instructions
**Check**: Verify test execution in workflow

## Best Practices

### ✅ Do
- Start every project with SPECS.md agreement
- Keep TODO.md current and actionable
- Review AI-generated documentation for accuracy
- Use approval gates for architectural decisions
- Combine instructions purposefully

### ❌ Don't
- Skip the specification phase
- Ignore TODO.md updates
- Accept changes without understanding them
- Mix conflicting instruction paradigms
- Override core protocol requirements

### 🎯 Pro Tips
- Use AIO instructions for rapid prototyping
- Combine protocol instructions for microservices
- Add utility instructions for workflow optimization
- Create custom instructions for team standards
- Regular review approval gate thresholds
