# Troubleshooting Guide

## Common Issues and Solutions

### Installation and Configuration Issues

#### Issue: Instructions Not Loading
**Symptoms:**
- AI doesn't follow development protocols
- No SPECS.md creation prompts
- Missing TODO.md updates

**Diagnosis:**
```bash
# Check VS Code settings
cat ~/.vscode/settings.json | grep -A 5 -B 5 "instructionsFilesLocations"

# Verify file paths exist
ls -la "/path/to/github_copilot_instructions_public/public/**/*.instructions.md"
```

**Solutions:**
1. **Verify File Paths**
   ```json
   {
     "chat.instructionsFilesLocations": [
       "/absolute/path/to/github_copilot_instructions_public/public/**/*.instructions.md"
     ]
   }
   ```

2. **Use Individual File Paths** (if glob patterns fail)
   ```json
   {
     "chat.instructionsFilesLocations": [
       "/path/to/core_dev.instructions.md",
       "/path/to/python_guide.instructions.md"
     ]
   }
   ```

3. **Restart VS Code** after configuration changes

#### Issue: Glob Pattern Not Working
**Symptoms:**
- Some instruction files load, others don't
- Inconsistent behavior

**Solutions:**
1. **Use Absolute Paths**
   ```bash
   # Find absolute path
   pwd
   # Use full path in VS Code settings
   ```

2. **Test Glob Pattern**
   ```bash
   # Verify glob expansion
   echo /path/to/github_copilot_instructions_public/public/**/*.instructions.md
   ```

3. **Alternative Pattern**
   ```json
   {
     "chat.instructionsFilesLocations": [
       "/path/to/github_copilot_instructions_public/public/core_behaviours/*.instructions.md",
       "/path/to/github_copilot_instructions_public/public/python/*.instructions.md"
     ]
   }
   ```

### Protocol Compliance Issues

#### Issue: AI Not Creating SPECS.md
**Symptoms:**
- AI starts coding immediately
- No specification agreement phase
- Missing project governance files

**Diagnosis:**
```bash
# Check if core development instructions are loaded
grep -r "SPECS.md" /path/to/instructions/
```

**Solutions:**
1. **Explicit Instruction Loading**
   ```json
   {
     "chat.instructionsFilesLocations": [
       "/path/to/core_dev.instructions.md"
     ]
   }
   ```

2. **Manual Protocol Initiation**
   ```
   User prompt: "Before we start, please follow the core development protocol and create .github/SPECS.md"
   ```

3. **Verify Core Instructions Content**
   ```bash
   cat /path/to/core_dev.instructions.md | head -20
   ```

#### Issue: Missing Approval Gates
**Symptoms:**
- Large changes implemented without approval requests
- No 50+ line threshold enforcement

**Solutions:**
1. **Reinforce Protocol**
   ```
   User prompt: "Please follow the approval gate protocol for changes over 50 lines"
   ```

2. **Check Instruction Precedence**
   - Ensure core_dev.instructions.md is first in configuration
   - Remove conflicting instructions that override approval gates

3. **Manual Gate Enforcement**
   ```
   User prompt: "Show me the proposed changes before implementing"
   ```

### Code Quality Issues

#### Issue: Inconsistent Code Style
**Symptoms:**
- Mixed coding patterns
- Inconsistent naming conventions
- Style violations

**Diagnosis:**
```bash
# Check which language instructions are loaded
ls /path/to/instructions/ | grep -E "(python|typescript)_guide"
```

**Solutions:**
1. **Ensure Language Guide Priority**
   ```json
   {
     "chat.instructionsFilesLocations": [
       "/path/to/core_dev.instructions.md",
       "/path/to/python_guide.instructions.md",  // Must be before specialized files
       "/path/to/python_api_development.instructions.md"
     ]
   }
   ```

2. **Add Best Practices Instructions**
   ```json
   {
     "chat.instructionsFilesLocations": [
       "/path/to/python_best_practices.instructions.md"
     ]
   }
   ```

#### Issue: Under-Testing
**Symptoms:**
- Missing test coverage
- No test-driven development
- Lack of integration tests

**Solutions:**
1. **Add Testing Instructions**
   ```json
   {
     "chat.instructionsFilesLocations": [
       "/path/to/python_testing_quality.instructions.md"
     ]
   }
   ```

2. **Explicit Testing Requirements**
   ```
   User prompt: "Please include comprehensive testing with unit, integration, and e2e tests"
   ```

### Integration Issues

#### Issue: Conflicting Instructions
**Symptoms:**
- AI provides contradictory guidance
- Inconsistent behavior across sessions
- Mixed paradigms in same project

**Diagnosis:**
```bash
# Check for overlapping instruction files
grep -r "similar_concept" /path/to/instructions/
```

**Solutions:**
1. **Review Instruction Hierarchy**
   - Follow precedence: Core → Language → Domain → Protocol → Quality → Utils
   - Remove conflicting specialized instructions

2. **Use Recommended Combinations**
   - See [Reference Guide](reference/README.md) for validated combinations
   - Avoid mixing AIO instructions with specialized ones

3. **Test Combination**
   ```bash
   # Create test project with specific instruction set
   mkdir test-project
   cd test-project
   # Test AI behavior with current configuration
   ```

#### Issue: Missing Dependencies
**Symptoms:**
- AI references undefined patterns
- Incomplete implementation guidance
- Missing integration points

**Solutions:**
1. **Check Dependency Chain**
   ```
   Domain instructions → Language guide → Core protocol
   ```

2. **Add Missing Dependencies**
   ```json
   {
     "chat.instructionsFilesLocations": [
       "/path/to/core_dev.instructions.md",
       "/path/to/python_guide.instructions.md",        // Required base
       "/path/to/python_api_development.instructions.md" // Depends on guide
     ]
   }
   ```

### Performance Issues

#### Issue: Slow AI Responses
**Symptoms:**
- Long delays in AI responses
- VS Code performance degradation
- Memory usage increases

**Solutions:**
1. **Reduce Instruction Load**
   ```json
   {
     "chat.instructionsFilesLocations": [
       // Use specific files instead of broad glob patterns
       "/path/to/essential.instructions.md"
     ]
   }
   ```

2. **Use AIO Instructions**
   ```json
   {
     "chat.instructionsFilesLocations": [
       "/path/to/python_api_service.instructions.md"  // Single comprehensive file
     ]
   }
   ```

3. **Monitor Resource Usage**
   ```bash
   # Check VS Code processes
   ps aux | grep "Code"
   ```

#### Issue: Context Overflow
**Symptoms:**
- AI loses context mid-conversation
- Inconsistent behavior in long sessions
- Incomplete responses

**Solutions:**
1. **Minimize Instruction Complexity**
   - Use simpler instruction combinations
   - Focus on essential instructions only

2. **Break Down Sessions**
   - Start new chat sessions for different features
   - Use clear, focused prompts

3. **Optimize Instruction Content**
   - Remove verbose instructions
   - Focus on actionable guidance

## Debugging Workflows

### Basic Diagnostic Checklist
- [ ] VS Code settings include correct instruction paths
- [ ] Instruction files exist at specified locations
- [ ] Core development instructions are loaded
- [ ] Language guide is included for target technology
- [ ] No conflicting instruction combinations

### Advanced Debugging

#### 1. Instruction Loading Verification
```bash
# Create test project
mkdir copilot-test && cd copilot-test

# Test with minimal instructions
echo '{"chat.instructionsFilesLocations": ["/path/to/core_dev.instructions.md"]}' > .vscode/settings.json

# Open in VS Code and test
code .
```

#### 2. Protocol Compliance Testing
```bash
# Test SPECS.md creation
# User prompt: "Create a Python API project"
# Expected: AI asks to create .github/SPECS.md first

# Test approval gates
# User prompt: "Implement a complex feature with 100+ lines"
# Expected: AI requests approval before implementation
```

#### 3. Integration Testing
```bash
# Test instruction combinations
for combination in "python-api" "typescript-frontend" "data-science"; do
  mkdir test-$combination
  cd test-$combination
  # Configure specific instruction set
  # Test AI behavior
  cd ..
done
```

### Performance Optimization

#### Instruction Set Optimization
```bash
# Measure instruction loading time
time code . # Note startup time

# Test different combinations
# Minimal set:
chat.instructionsFilesLocations: ["core_dev.instructions.md"]

# Full set:
chat.instructionsFilesLocations: ["public/**/*.instructions.md"]

# Compare performance
```

#### Memory Management
```bash
# Monitor VS Code memory usage
while true; do
  ps aux | grep "Visual Studio Code" | grep -v grep
  sleep 10
done
```

## FAQ

### Q: Can I use multiple language instructions simultaneously?
**A:** Yes, when working on multi-language projects. The AI will apply appropriate guidance based on file context.

### Q: How do I override specific instruction behaviors?
**A:** Create custom instructions in the `user/` directory with higher precedence, or use more specific instruction files.

### Q: What if my team has different coding standards?
**A:** Create team-specific instruction files that extend or override the public instructions while maintaining core protocol compliance.

### Q: Can I disable the approval gates for rapid prototyping?
**A:** Use AIO (All-in-One) instructions which have streamlined approval processes, or create custom instructions with modified thresholds.

### Q: How do I update instructions when new versions are released?
**A:** Pull the latest repository changes and restart VS Code. Instructions are loaded fresh each session.

### Q: Can I contribute fixes for issues I encounter?
**A:** Yes! Follow the [Development Guide](development-guide.md) for contribution guidelines.

## Getting Help

### Community Support
- GitHub Issues: Report bugs and request features
- Discussions: Ask questions and share experiences
- Wiki: Community-maintained troubleshooting knowledge

### Documentation References
- [Architecture Guide](architecture.md): Understanding instruction relationships
- [User Guide](user-guide.md): Effective usage patterns
- [Reference Guide](reference/README.md): Complete instruction catalog

### Emergency Procedures

#### Complete Reset
```bash
# Backup current settings
cp ~/.vscode/settings.json ~/.vscode/settings.json.backup

# Remove all instruction configurations
# Edit settings.json to remove instructionsFilesLocations

# Restart VS Code
# Test basic Copilot functionality

# Gradually re-add instructions one by one
```

#### Minimal Working Configuration
```json
{
  "chat.instructionsFilesLocations": [
    "/path/to/core_dev.instructions.md"
  ]
}
```

Start with this minimal configuration and add instructions incrementally to identify problematic combinations.
