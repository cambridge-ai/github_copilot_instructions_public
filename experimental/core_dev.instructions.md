# Core Development Protocol

## 1. Project Initialization

### Specification Agreement
- **MANDATORY**: Establish `.github/SPECS.md` with user approval before any development
- **VALIDATION**: All subsequent work must align with approved specifications

### Task Management
- **CREATE**: `.github/TODO.md` as living task registry
- **MAINTAIN**: Update TODO after every code change
- **STRUCTURE**: Organize tasks by priority and dependency

## 2. Code Quality Standards

### Modularity Requirements
- **PRINCIPLE**: Design for readability and maintainability
- **ENFORCEMENT**: Break complex functions into smaller, reusable components
- **REVIEW**: Assess coupling and cohesion before implementation

### Testing Protocol
- **COVERAGE**: Implement multi-level test suite:
  - Unit tests (function/method level)
  - Integration tests (component interaction)
  - End-to-end tests (user workflow)
- **EXECUTION**: Run relevant tests before any commit
- **MAINTENANCE**: Update tests when modifying functionality

## 3. Change Management

### Approval Gates
- **THRESHOLD**: Changes ≥50 lines require user approval
- **PROCESS**: 
  1. Present proposed changes
  2. Wait for explicit user confirmation
  3. Proceed only after approval received
- **DOCUMENTATION**: Log approval decisions in commit messages

### Documentation Standards
- **PRIMARY**: Maintain comprehensive `/docs` directory
- **OVERVIEW**: Keep `README.md` high-level, referencing `/docs` for details
- **SYNCHRONIZATION**: Update documentation with every functional change
- **VALIDATION**: Ensure documentation accuracy before marking tasks complete

## 4. Execution Checklist

For every development iteration:
- [ ] Verify alignment with `.github/SPECS.md`
- [ ] Update `.github/TODO.md` with completed/pending tasks
- [ ] Implement modular, testable code
- [ ] Execute appropriate test levels
- [ ] Obtain approval for major changes (≥50 lines)
- [ ] Update `/docs` documentation
- [ ] Validate documentation accuracy