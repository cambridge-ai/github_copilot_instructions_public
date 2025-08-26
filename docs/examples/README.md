# Examples and Use Cases

## Real-World Project Scenarios

### 1. E-commerce API Development

**Scenario**: Building a complete e-commerce REST API with user management, product catalog, and order processing.

**Instruction Configuration**:
```
core_dev.instructions.md (automatic)
python_guide.instructions.md
python_api_development.instructions.md
rest_api.instructions.md
python_testing_quality.instructions.md
```

**Project Setup Flow**:
```markdown
1. User: "I want to build an e-commerce API with FastAPI"
2. AI: "Let's establish .github/SPECS.md first..."
3. SPECS.md created with requirements
4. .github/TODO.md initialized with tasks
5. Development proceeds with approval gates
```

**Expected Outcomes**:
- Modular FastAPI application structure
- Comprehensive test suite (unit, integration, e2e)
- RESTful API design patterns
- Automatic documentation generation
- Production-ready deployment configuration

### 2. React Dashboard Application

**Scenario**: Modern dashboard application with real-time data visualization and user authentication.

**Instruction Configuration**:
```
core_dev.instructions.md (automatic)
typescript_guide.instructions.md
typescript_web_frontend.instructions.md
typescript_testing_quality.instructions.md
```

**Project Workflow**:
```markdown
1. Specification phase: Define dashboard requirements
2. Component architecture planning
3. State management strategy
4. API integration patterns
5. Testing strategy implementation
```

**Generated Structure**:
```
src/
├── components/           # Reusable UI components
├── pages/               # Route-based page components
├── hooks/               # Custom React hooks
├── services/            # API integration
├── store/               # State management
├── types/               # TypeScript definitions
└── utils/               # Utility functions
tests/
├── unit/                # Component unit tests
├── integration/         # Feature integration tests
└── e2e/                 # End-to-end user flows
```

### 3. Data Science Pipeline

**Scenario**: Machine learning pipeline for customer churn prediction with automated model training and evaluation.

**Instruction Configuration**:
```
core_dev.instructions.md (automatic)
python_guide.instructions.md
python_data_science.instructions.md
python_testing_quality.instructions.md
```

**Development Pattern**:
```python
# AI-guided structure following data science best practices
notebooks/
├── 01_data_exploration.ipynb
├── 02_feature_engineering.ipynb
├── 03_model_training.ipynb
└── 04_model_evaluation.ipynb

src/
├── data/                # Data processing modules
├── features/            # Feature engineering
├── models/              # Model implementations
└── evaluation/          # Model evaluation tools
```

### 4. Microservices Architecture

**Scenario**: Multi-service application with user service, product service, and API gateway.

**Per-Service Configuration**:
```
# User Service (Python)
core_dev.instructions.md
python_guide.instructions.md
python_api_development.instructions.md
rest_api.instructions.md
a2a.instructions.md
python_testing_quality.instructions.md

# Product Service (TypeScript)
core_dev.instructions.md
typescript_guide.instructions.md
typescript_api_development.instructions.md
rest_api.instructions.md
a2a.instructions.md
typescript_testing_quality.instructions.md

# API Gateway (TypeScript)
core_dev.instructions.md
typescript_guide.instructions.md
typescript_backend.instructions.md
rest_api.instructions.md
```

**Cross-Service Coordination**:
```
project_management.instructions.md (for overall coordination)
```

### 5. AI Agent System

**Scenario**: Multi-agent system with specialized agents for different tasks, using Model Context Protocol.

**Instruction Configuration**:
```
core_dev.instructions.md (automatic)
python_guide.instructions.md
agent.instructions.md
mcp.instructions.md
a2a.instructions.md
python_testing_quality.instructions.md
```

**Agent Architecture**:
```python
agents/
├── coordinator/         # Main coordination agent
├── data_analyst/        # Data analysis specialist
├── content_creator/     # Content generation agent
└── quality_assessor/    # Quality validation agent

protocols/
├── mcp_integration/     # Model Context Protocol implementation
└── agent_communication/ # Inter-agent communication
```

## Configuration Templates

### Startup Project Template
```json
{
  "name": "startup-mvp",
  "instructions": [
    "core_dev.instructions.md",
    "python_api_service.instructions.md"  // AIO for rapid development
  ],
  "description": "Rapid MVP development with opinionated stack"
}
```

### Enterprise Project Template
```json
{
  "name": "enterprise-application",
  "instructions": [
    "core_dev.instructions.md",
    "typescript_guide.instructions.md",
    "typescript_full_stack.instructions.md",
    "rest_api.instructions.md",
    "typescript_testing_quality.instructions.md",
    "project_management.instructions.md"
  ],
  "description": "Production-ready enterprise application"
}
```

### Research Project Template
```json
{
  "name": "research-project",
  "instructions": [
    "core_dev.instructions.md",
    "python_guide.instructions.md",
    "python_data_science.instructions.md",
    "python_testing_quality.instructions.md"
  ],
  "description": "Reproducible research with proper documentation"
}
```

## Common Patterns and Solutions

### Pattern: API-First Development

**Problem**: Building frontend and backend simultaneously with consistent API contracts.

**Solution**:
```
1. Start with API specification in SPECS.md
2. Use rest_api.instructions.md for consistent patterns
3. Generate OpenAPI documentation
4. Frontend consumes documented API
```

**Configuration**:
```
Backend: python_api_development.instructions.md + rest_api.instructions.md
Frontend: typescript_web_frontend.instructions.md + rest_api.instructions.md
```

### Pattern: Test-Driven Development

**Problem**: Ensuring comprehensive test coverage and quality.

**Solution**:
```
1. Include testing_quality.instructions.md
2. AI writes tests before implementation
3. Continuous integration with quality gates
4. Multiple test levels (unit, integration, e2e)
```

**Expected Behavior**:
```python
# AI-generated test-first approach
def test_user_creation_with_valid_data():
    """Test user creation with valid input data."""
    # Arrange
    user_data = {"name": "John Doe", "email": "john@example.com"}
    
    # Act
    result = create_user(user_data)
    
    # Assert
    assert result.success is True
    assert result.user.id is not None

# Implementation follows to make test pass
def create_user(user_data):
    # Implementation guided by test requirements
    pass
```

### Pattern: Modular Architecture

**Problem**: Maintaining code organization and reusability.

**Solution**:
```
1. Core development protocol enforces modularity
2. Language guides provide specific patterns
3. Regular refactoring for maintainability
```

**AI Guidance**:
```python
# AI suggests modular structure
# Instead of monolithic function:
def process_order(order_data):
    # 100+ lines of mixed logic
    pass

# AI recommends:
def process_order(order_data):
    validated_order = validate_order(order_data)
    inventory_check = verify_inventory(validated_order)
    payment_result = process_payment(inventory_check)
    return finalize_order(payment_result)
```

### Pattern: Documentation-Driven Development

**Problem**: Keeping documentation current and comprehensive.

**Solution**:
```
1. Core protocol requires documentation updates
2. AI maintains /docs automatically
3. High-level README references detailed docs
```

**Generated Documentation**:
```
/docs/
├── README.md           # Documentation index
├── api.md             # API documentation
├── architecture.md    # System design
├── setup.md           # Installation guide
└── contributing.md    # Development guide
```

## Troubleshooting Examples

### Example: Mixed Technology Stack

**Problem**: Working with Python backend and TypeScript frontend in same repository.

**Solution**:
```
# Root configuration includes both language guides
instructions:
  - core_dev.instructions.md
  - python_guide.instructions.md
  - typescript_guide.instructions.md
  - python_api_development.instructions.md
  - typescript_web_frontend.instructions.md
  - rest_api.instructions.md
```

**AI Behavior**: Recognizes context and applies appropriate language-specific guidance based on file being edited.

### Example: Performance Optimization Project

**Problem**: Existing application needs performance improvements.

**Enhanced Configuration**:
```
core_dev.instructions.md
{language}_guide.instructions.md
{language}_best_practices.instructions.md  # Advanced patterns
{language}_testing_quality.instructions.md
```

**AI Focus**: Emphasis on performance testing, profiling, and optimization patterns.

### Example: Legacy Code Migration

**Problem**: Modernizing legacy codebase to current standards.

**Migration Strategy**:
```
1. Document current state in SPECS.md
2. Create migration plan in TODO.md
3. Use approval gates for architectural changes
4. Maintain comprehensive test coverage during migration
```

**AI Guidance**: Suggests incremental migration patterns while maintaining functionality.

## Success Metrics

### Project Quality Indicators
- **Documentation Coverage**: All major features documented
- **Test Coverage**: >90% code coverage across test levels
- **Code Quality**: Passes all linting and type checking
- **Architecture**: Modular, maintainable structure
- **Process Compliance**: Follows core development protocol

### Development Velocity Indicators
- **Setup Time**: Project ready for development <30 minutes
- **Feature Development**: Consistent velocity with quality gates
- **Deployment**: Automated, reliable deployment process
- **Maintenance**: Easy to onboard new developers

### AI Effectiveness Indicators
- **Protocol Adherence**: AI consistently follows development protocol
- **Code Quality**: Generated code meets quality standards
- **Documentation**: Auto-generated docs are accurate and helpful
- **Testing**: Comprehensive test generation and execution
