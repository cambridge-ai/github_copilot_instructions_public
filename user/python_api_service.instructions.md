# Python API Service Development Instructions

## Core Development Philosophy

### 1. MVP-First Approach
- **Build core functionalities only** - Focus on the essential features that make the API functional
- **Avoid feature creep** - Do not assume or implement features beyond the developer's explicit instructions
- **Simple implementations first** - Choose the most straightforward approach that meets requirements
- **Defer optimizations** - Implement working solutions before considering performance improvements

### 2. Specification-Driven Development
- **Create SPECS.md first** - Always start by creating a detailed specification document
- **Finalize specs with developer** - Review and confirm all requirements before coding begins
- **Reference specs throughout development** - Ensure all implementations align with agreed specifications
- **Update specs when requirements change** - Keep documentation current with any modifications

### 3. Incremental Development Process
- **Maintain TODO.md** - Keep a prioritized list of tasks aligned with SPECS.md
- **Update TODO after each completion** - Mark completed tasks and adjust priorities
- **Git commits per major functionality** - Prompt developer to commit after each significant feature
- **One functionality at a time** - Complete and test each feature before moving to the next

### 4. Agile Function-First Development
- **Build reusable functions first** - Create small, testable functions as building blocks
- **Compose functions into features** - Combine simple functions to create larger functionalities
- **Test functions independently** - Ensure each function works correctly in isolation
- **Refactor when composing** - Improve function interfaces when building larger components

## Development Workflow

### Phase 1: Planning and Specification
1. **Create SPECS.md** with:
   - API endpoints and methods
   - Data models and schemas
   - Authentication requirements
   - Business logic requirements
   - Success criteria for MVP

2. **Create TODO.md** with:
   - Prioritized task breakdown
   - Dependencies between tasks
   - Estimated complexity levels
   - Completion checkboxes

3. **Review with developer** - Confirm understanding before coding

### Phase 2: Foundation Setup
1. **Project structure** - Set up basic Python project layout
2. **Dependencies** - Install minimal required packages
3. **Configuration** - Basic settings and environment handling
4. **Git commit** - "Initial project setup"

### Phase 3: Core Function Development
1. **Data models** - Define core data structures
2. **Utility functions** - Build helper functions for common operations
3. **Business logic functions** - Implement core business rules
4. **Git commit** - "Core functions implemented"

### Phase 4: API Layer Development
1. **Route handlers** - Create endpoint handlers using core functions
2. **Request/response handling** - Implement data validation and serialization
3. **Error handling** - Add basic error responses
4. **Git commit** - "API endpoints implemented"

### Phase 5: Integration and Testing
1. **Integration testing** - Test complete request/response cycles
2. **Error case testing** - Verify error handling works correctly
3. **Documentation** - Update API documentation
4. **Git commit** - "MVP complete and tested"

## Technical Guidelines

### API Framework Choice
- **FastAPI** (recommended) - For modern, async APIs with automatic documentation
- **Flask** - For simple, straightforward APIs
- **Django REST Framework** - For complex APIs with built-in admin features

### Project Structure
```
project_name/
├── SPECS.md
├── TODO.md
├── README.md
├── requirements.txt
├── .env.example
├── app/
│   ├── __init__.py
│   ├── main.py
│   ├── models/
│   ├── services/
│   ├── routes/
│   └── utils/
└── tests/
```

### Function Design Principles
1. **Single responsibility** - Each function should do one thing well
2. **Pure functions preferred** - Avoid side effects when possible
3. **Clear inputs/outputs** - Use type hints and docstrings
4. **Error handling** - Return results or raise specific exceptions
5. **Testable** - Write functions that are easy to unit test

### Code Quality Standards
- **Type hints** - Use Python type annotations
- **Docstrings** - Document all functions and classes
- **Error handling** - Proper exception handling and logging
- **Input validation** - Validate all inputs at API boundaries
- **Consistent naming** - Follow Python naming conventions

## Communication Guidelines

### When to Ask Questions
- **Unclear requirements** - If specifications are ambiguous
- **Multiple implementation options** - When there are valid alternatives
- **Scope boundaries** - If unsure whether a feature should be included
- **Technical constraints** - When facing implementation challenges
- **Priority conflicts** - If TODO items need reordering

### Question Format
- **Be specific** - Ask about particular aspects, not general preferences
- **Provide context** - Explain why the question arose
- **Offer options** - Present 2-3 potential approaches when possible
- **Impact assessment** - Explain how the choice affects other features

### Progress Updates
- **Before major changes** - Confirm approach before significant work
- **After completions** - Report when TODO items are finished
- **When blocked** - Immediately report any blockers or issues
- **At commit points** - Summarize what was accomplished

## Example Development Session

### 1. Initial Planning
```
Developer: I need an API for managing user tasks
Agent: I'll create SPECS.md to define the requirements. Let me confirm:
- User authentication needed?
- Task properties (title, description, due date, status)?
- Required endpoints (CRUD operations)?
- Any specific business rules?
```

### 2. Specification Creation
```
Agent: Created SPECS.md with:
- POST /auth/login - User authentication
- GET/POST/PUT/DELETE /tasks - Task CRUD operations
- Task model: id, title, description, due_date, status, user_id
- JWT authentication for all task endpoints

Please review SPECS.md. Should I proceed with TODO.md creation?
```

### 3. Implementation Start
```
Agent: Created TODO.md with prioritized tasks:
1. [ ] Set up FastAPI project structure
2. [ ] Create User and Task models
3. [ ] Implement authentication functions
4. [ ] Create task management functions
5. [ ] Build API endpoints
6. [ ] Add error handling
7. [ ] Write tests

Ready to start with project setup?
```

### 4. Incremental Development
```
Agent: Completed project setup and basic models.
Core functions implemented:
- create_user()
- authenticate_user()
- create_task()
- get_user_tasks()

Ready for git commit: "Core functions implemented"
Shall I proceed with API endpoint creation?
```

## Error Handling Strategy

### Function Level
- **Return Result objects** - Use success/error result patterns
- **Specific exceptions** - Create custom exception classes
- **Input validation** - Check parameters at function entry
- **Logging** - Log errors with context information

### API Level
- **HTTP status codes** - Use appropriate status codes
- **Error response format** - Consistent error message structure
- **Validation errors** - Clear field-specific error messages
- **Internal error handling** - Don't expose internal details

## Testing Approach

### Unit Testing
- **Test functions independently** - Mock external dependencies
- **Test edge cases** - Include boundary conditions and error cases
- **Test data validation** - Verify input validation works
- **Use pytest** - Recommended testing framework

### Integration Testing
- **Test complete workflows** - End-to-end request/response cycles
- **Test error scenarios** - Verify error handling in full context
- **Test authentication** - Verify security measures work
- **Use test database** - Isolated test environment

## Documentation Requirements

### Code Documentation
- **Function docstrings** - Describe purpose, parameters, returns
- **Type hints** - Use Python type annotations
- **Inline comments** - Explain complex business logic
- **API documentation** - Auto-generated from code when possible

### Project Documentation
- **SPECS.md** - Detailed technical specifications
- **TODO.md** - Current task status and priorities
- **README.md** - Setup and usage instructions
- **API documentation** - Endpoint details and examples

Remember: Always prioritize working software over comprehensive documentation, but maintain enough documentation for project continuity and developer understanding.