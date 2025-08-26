# Development Guide

## Contributing to GitHub Copilot Instructions

### Prerequisites
- Understanding of GitHub Copilot Agent Mode
- Experience with the target technology/domain
- Familiarity with the [Core Development Protocol](../public/core_behaviours/core_dev.instructions.md)

### Development Workflow

#### 1. Planning Phase
```bash
# Follow the core protocol
git checkout -b feature/new-instruction
echo "Create .github/SPECS.md for new instruction file" >> .github/TODO.md
```

#### 2. Specification Development
Create `.github/SPECS.md` with:
```markdown
# New Instruction File Specification

## Purpose
[Clear statement of instruction file purpose]

## Target Technology
[Technology, framework, or domain covered]

## Scope
[What the instruction file will and won't cover]

## Integration Points
[How it relates to existing instruction files]

## Success Criteria
[Measurable outcomes for effectiveness]
```

#### 3. Implementation Standards

##### File Structure Template
```markdown
# [Technology/Domain] Instructions

## Core Principles
[Fundamental concepts and approaches]

## Development Standards
[Specific coding standards and practices]

## Technology Stack
[Current recommended versions and tools]

## Web Search Integration
[Instructions for staying current with latest developments]

## Implementation Patterns
[Specific code patterns and examples]

## Quality Assurance
[Testing and validation requirements]

## Integration Guidelines
[How to combine with other instruction files]
```

##### Required Sections
1. **Web Search Capabilities**: Every instruction file must include guidance for staying current
2. **Technology Currency**: Mechanisms for tracking latest versions and trends
3. **Integration Patterns**: How to combine with other instructions
4. **Quality Standards**: Testing and validation requirements

### Instruction File Categories

#### Language-Specific Instructions
**Purpose**: Foundation for technology stack
**Requirements**:
- Comprehensive language coverage
- Framework recommendations
- Tooling and environment setup
- Best practices and patterns

**Template**: Use `python_guide.instructions.md` or `typescript_guide.instructions.md` as reference

#### Domain-Specific Instructions
**Purpose**: Specialized use case guidance
**Requirements**:
- Build on language foundation
- Domain-specific patterns
- Integration with relevant protocols
- Quality standards for domain

**Examples**: API development, web development, data science

#### Protocol Instructions
**Purpose**: Communication and integration patterns
**Requirements**:
- Technology-agnostic when possible
- Clear implementation guidelines
- Integration with language-specific files
- Current protocol specifications

**Examples**: REST API, MCP, Agent-to-Agent

#### AIO (All-in-One) Instructions
**Purpose**: Opinionated, complete application stacks
**Requirements**:
- Production-ready patterns
- Comprehensive technology stack
- Minimal configuration decisions
- Integrated tooling setup

**Examples**: NestJS API Service, React Frontend Application

### Quality Standards

#### Content Requirements
- **Actionable**: Every instruction must be implementable
- **Current**: Include mechanisms for staying up-to-date
- **Testable**: Provide validation criteria
- **Modular**: Work independently and in combination

#### Technical Validation
```bash
# Lint instruction files
markdownlint *.instructions.md

# Validate structure
./scripts/validate-instruction-structure.sh

# Test combinations
./scripts/test-instruction-combinations.sh
```

#### Testing Protocol
1. **Unit Testing**: Individual instruction file effectiveness
2. **Integration Testing**: Combination with other instructions
3. **User Testing**: Real-world scenario validation
4. **Regression Testing**: Ensure no conflicts with existing files

### Review Process

#### Pull Request Requirements
- [ ] `.github/SPECS.md` updated with new instruction specification
- [ ] `.github/TODO.md` updated with completed tasks
- [ ] New instruction file follows template structure
- [ ] Documentation updated in `/docs`
- [ ] Integration testing completed
- [ ] User guide examples added

#### Review Criteria
1. **Completeness**: Covers stated scope thoroughly
2. **Accuracy**: Technical information is correct and current
3. **Clarity**: Instructions are clear and actionable
4. **Integration**: Works well with existing instruction files
5. **Maintenance**: Includes currency and update mechanisms

### Maintenance Guidelines

#### Regular Updates
- **Monthly**: Check for new technology releases
- **Quarterly**: Review and update best practices
- **Annually**: Comprehensive instruction file audit

#### Version Management
- Semantic versioning for major instruction changes
- Change logs for significant updates
- Migration guides for breaking changes

#### Community Feedback
- Issue tracking for instruction effectiveness
- User feedback integration
- Regular effectiveness audits

## Advanced Development Patterns

### Meta-Instruction Development
Creating instructions that help develop other instructions:
- Instruction generation patterns
- Quality validation automation
- Integration testing frameworks

### Domain Extension
Adding new technology domains:
1. Research domain-specific requirements
2. Identify integration points with existing instructions
3. Develop comprehensive coverage plan
4. Create specialized testing protocols

### Protocol Evolution
Updating communication protocol instructions:
1. Monitor protocol specification changes
2. Test backward compatibility
3. Provide migration guidance
4. Update dependent instruction files

## Tools and Automation

### Development Scripts
```bash
# Generate new instruction file template
./scripts/generate-instruction-template.sh <type> <name>

# Validate instruction file structure
./scripts/validate-instruction.sh <file>

# Test instruction combinations
./scripts/test-combinations.sh <instruction-set>

# Update technology currency checks
./scripts/update-currency-checks.sh
```

### Integration Testing
```bash
# Test with real projects
./tests/integration/test-python-api.sh
./tests/integration/test-typescript-frontend.sh
./tests/integration/test-aio-combinations.sh
```

### Quality Metrics
- Instruction effectiveness scores
- User satisfaction ratings
- Technology currency metrics
- Integration success rates

## Release Process

### Pre-Release Checklist
- [ ] All tests passing
- [ ] Documentation updated
- [ ] Examples validated
- [ ] Integration testing completed
- [ ] Review process completed

### Release Steps
1. Update version numbers
2. Generate changelog
3. Tag release
4. Update documentation
5. Announce changes

### Post-Release
1. Monitor user feedback
2. Track effectiveness metrics
3. Plan next iteration
4. Address urgent issues
