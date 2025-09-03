# Claude Code Guide

## 📋 Learning Path Overview

This guide is structured for progressive learning, from basic usage to expert-level workflows:

**📍 Foundation Level**

- Quick Start - Get Claude Code running in 30 seconds
- Essential Commands - Core commands for daily use
- Project Setup - Initialize your first project properly

**📍 Intermediate Level**

- Plan Mode Mastery - Leverage Claude's most powerful feature
- Response Optimization - Get better results from your prompts
- Safe Workflows - Professional practices with risk mitigation

**📍 Advanced Level**

- Parallel Sessions - Multi-terminal productivity workflows
- Project Creation - Building new projects from scratch
- Automation & Integration - Expert patterns and troubleshooting
- MCP integration & use cases
- Subagents integration & use cases
- Learning mode explained

---

## 🚀 Quick Start

*Get up and running with Claude Code in 30 seconds*

```bash
# Install Claude Code globally
npm install -g @anthropic-ai/claude-code

# Navigate to your project
cd your-project

# Start Claude Code
claude
# You'll be prompted to log in on first use
```

**Authentication Options:**

- **Claude Pro/Max subscription** (recommended for regular use)
- **Anthropic API** (pay-per-use, good for occasional use)

**Core Philosophy:** Claude Code is an agentic coding tool that lives in your terminal and helps you turn ideas into code faster than ever before, designed with the Unix philosophy: composable and scriptable.

---

## 📚 Essential Commands

*Master the core commands you'll use daily*

### **Starting and Managing Sessions**

```bash
claude                    # Start interactive session
claude -p "your prompt"   # One-shot command (headless mode)
/help                     # Show all available commands
/clear                    # Clear conversation history (use frequently!)
/quit                     # Exit Claude Code session
```

### **Project Initialization (Critical First Steps)**

```bash
/init                     # Analyze codebase and create CLAUDE.md (run first!)
/ide                      # Connect to VS Code/Cursor for file awareness
/terminal-setup           # Optimize terminal for Claude Code
```

### **Context Management**

```bash
/model                    # Switch between Sonnet and Opus
/permissions              # Manage tool permissions
/cost                     # Check token usage and costs
/add-dir path/to/dir      # Add additional working directories
```

### **Development Workflow**

```bash
/review                   # Comprehensive code review
/undo                     # Undo the last change
/save filename            # Save conversation to file
/load filename            # Load conversation from file
```

---

## 🏗️ Project Setup

*Essential setup for every Claude Code project*

### **Step 1: Initialize Your Project**

```bash
# In your project directory
claude
/init
```

This creates a CLAUDE.md file - your project's memory that persists across sessions.

### **Step 2: Create Your CLAUDE.md**

Claude will generate a basic CLAUDE.md, but customize it for maximum effectiveness:

```markdown
# CLAUDE.md

## PROJECT OVERVIEW
[Brief project description and current status]

## CRITICAL PATTERNS
- ALWAYS validate user inputs before processing
- NEVER expose sensitive data in error messages  
- OPTIMIZE for user-perceived performance
- MAINTAIN backward compatibility unless explicitly breaking

## ESSENTIAL COMMANDS
- `npm run dev` - Start development environment
- `npm run test` - Run full test suite
- `npm run build` - Production build
- `npm run lint` - Code quality checks

## ARCHITECTURE DECISIONS
- Database: [choice] because [specific reasoning]
- State management: [choice] because [specific reasoning]
- Authentication: [choice] because [specific reasoning]

## CODING STANDARDS
- Implement proper error boundaries and handling
- Include loading states for all async operations
- Follow existing naming conventions in codebase
```

### **Step 3: Configure Permissions**

```bash
/permissions
# Add essential tools: Edit, Bash, WebFetch
```

---

## 🧠 Plan Mode Mastery

*Claude Code's most powerful feature for complex tasks*

Plan Mode creates detailed implementation plans before coding, dramatically improving results for complex work.

### **How to Activate Plan Mode**

**Method 1: Direct Command**

```bash
/plan
"Build a user authentication system with email verification"
```

**Method 2: Natural Language Triggers**

```bash
"Think about implementing..."     # Basic planning
"Think hard about..."            # Extended planning  
"Think harder about..."          # Deep planning
"Ultrathink about..."           # Maximum planning
```

**Method 3: CLI Flag**

```bash
claude -p "your request" --plan-mode
```

### **Planning Budget Levels**

```bash
"think"        # 2-3 minutes of planning
"think hard"   # 5-8 minutes of planning
"think harder" # 10-15 minutes of planning
"ultrathink"   # 20+ minutes of planning
```

### **Writing Effective Planning Prompts**

**❌ Poor Planning Requests:**

- "Add authentication"
- "Make it faster"
- "Fix the bug"

**✅ Excellent Planning Requests:**

```bash
"Think hard about implementing user authentication with the following requirements:
- Email/password login with verification
- Social login (Google, GitHub)
- Password reset flow
- Session management with JWT
- Rate limiting for security
- Integration with existing user database
Plan the complete architecture, database changes, API endpoints, and security considerations."
```

### **Planning Best Practices**

1. **Be Extremely Specific**
   - Include all requirements and constraints
   - Specify performance and scale expectations
   - Mention integration points and dependencies

2. **Include Context and Constraints**
   - Current system limitations
   - Timeline and resource constraints
   - Technical debt considerations

3. **Request Verification**
   - Ask Claude to verify the plan addresses all requirements
   - Request consideration of edge cases and failure scenarios

---

## 💡 Response Optimization

*Techniques to get significantly better results from Claude Code*

### **Context-Rich Prompting**

**❌ Vague Request:**

```bash
"Fix this component"
```

**✅ Context-Rich Request:**

```bash
"This React component in @components/UserProfile.tsx is causing memory leaks when users navigate away quickly. The useEffect hook for fetching user data doesn't clean up properly. Fix the cleanup logic and add proper loading states."
```

### **Structured Output Requests**

**❌ Generic Request:**

```bash
"Review this code"
```

**✅ Structured Request:**

```bash
"Review @api/auth.js and provide:
1. Security vulnerabilities with severity levels
2. Performance optimizations with expected impact
3. Code maintainability improvements
4. Specific line-by-line suggestions with reasoning
Format as a structured report with priorities."
```

### **Success Criteria Definition**

**❌ Open-ended:**

```bash
"Optimize the database queries"
```

**✅ Success Criteria Defined:**

```bash
"Optimize the user dashboard queries in @lib/db.js to:
- Reduce load time from 3s to under 1s
- Handle 1000+ concurrent users
- Maintain data accuracy and consistency
- Preserve existing API contract
Measure before/after performance and confirm all tests pass."
```

### **Quality Enhancement Techniques**

**Request Multiple Alternatives:**

```bash
"Show me 3 different approaches to implement user notifications:
1. Real-time WebSocket approach
2. Polling-based approach  
3. Server-sent events approach
Compare pros/cons for a system with 10k users and limited server resources."
```

**Include Testing Requirements:**

```bash
"Implement this feature AND create comprehensive tests that cover:
- Happy path scenarios
- Edge cases and error conditions
- Performance under load
- Security vulnerabilities
Include both unit tests and integration tests."
```

---

## 🛡️ Safe Workflows

*Good practices to prevent accidents and maintain code quality*

### **Safe Permission Management**

Claude Code asks permission for every potentially dangerous action. Here's how to manage this professionally:

**Development Branch Strategy (Recommended)**

```bash
# Create dedicated development branches for AI-assisted work
git checkout -b feature/ai-development
git checkout -b experiment/claude-refactor

# Use skip permissions ONLY on these branches
claude --dangerously-skip-permissions

# Benefits:
# - Main/production code remains protected
# - Easy rollback if AI makes unwanted changes
# - Safe experimentation environment
# - Clear separation of AI-generated vs human-reviewed code
```

**Branch-Specific Workflow:**

```bash
# 1. Create AI development branch
git checkout -b ai/user-authentication
claude --dangerously-skip-permissions
"Implement user authentication system"

# 2. Review changes before merging
git diff main...ai/user-authentication

# 3. Merge only after human review
git checkout main
git merge ai/user-authentication  # Only after review
```

**Alternative: Controlled Permission Sets**

```bash
# For production branches, use controlled permissions
claude --allowedTools Edit,Bash(git:*,npm:*,test:*)
# This allows file editing and safe commands only
```

### **Safe Development Practices**

**1. Regular Backup Points**

```bash
# Create save points before major changes
git add . && git commit -m "Checkpoint before AI refactor"
claude --dangerously-skip-permissions
"Refactor the authentication system"
```

**2. Incremental Changes**

```bash
# Break large changes into reviewable chunks
"First, just refactor the user model validation"
# Review and commit
"Now refactor the authentication middleware"  
# Review and commit
"Finally, update the API endpoints"
```

**3. Continuous Validation**

```bash
# After each significant change
"Run all tests and ensure they pass before continuing"
"Check that the application still builds successfully"
"Verify no breaking changes in the API contract"
```

### **Risk Mitigation Strategies**

**Pre-Change Safety Checks:**

```bash
"Before making any changes:
1. Run the full test suite to establish baseline
2. Create a git checkpoint
3. Document current system behavior
4. Identify rollback procedure if needed"
```

**Post-Change Validation:**

```bash
"After implementing changes:
1. Run full test suite and compare with baseline
2. Test critical user paths manually
3. Check performance hasn't degraded
4. Verify no security vulnerabilities introduced
5. Document changes made and reasoning"
```

---

## ⚡ Parallel Sessions

*Multi-terminal workflows for maximum productivity*

Parallel sessions allow you to work on different aspects of your project simultaneously without context switching delays.

### **Basic Multi-Terminal Setup**

```bash
# Terminal 1: Main Development
cd /path/to/project
claude
# Focus: Feature implementation and core development work

# Terminal 2: Testing & Quality Assurance  
cd /path/to/project
claude --model sonnet  # Use faster model for testing
# Focus: Writing tests, running test suites, code quality checks

# Terminal 3: Documentation & Review
cd /path/to/project  
claude --plan-mode
# Focus: Documentation, code review, planning next steps
```

### **Git Worktree Parallel Development**

For completely independent features:

```bash
# Create separate worktrees for parallel features
git worktree add ../project-auth-feature auth-system
git worktree add ../project-payments-feature payment-integration

# Terminal 1: Authentication system
cd ../project-auth-feature
claude --dangerously-skip-permissions  # Safe in isolated branch
"Implement user authentication with session management"

# Terminal 2: Payment integration
cd ../project-payments-feature  
claude --dangerously-skip-permissions  # Safe in isolated branch
"Build subscription billing system with Stripe"
```

### **Session Coordination Techniques**

**Shared Context Management:**

```bash
# Terminal 1:
/save team-feature-implementation
"Core team feature is complete"

# Terminal 2:
/load team-feature-implementation  
"Now implement the frontend integration for the team feature"
```

**Cross-Session Communication:**

```bash
# Use shared files for coordination
# Terminal 1:
"Create a TODO.md file with current implementation status and next steps"

# Terminal 2:
"Read @TODO.md and work on the next priority item"
```

---

## 🏗️ Creating Projects from Zero

*Project initialization and template creation*

### **Project Planning Workflow**

**Step 1: Requirements Analysis**

```bash
"Ultrathink about creating a [project type] with these requirements:
- Target users: [description]
- Core functionality: [list features]
- Technical constraints: [limitations]
- Performance requirements: [specifications]
- Timeline: [deadline]
Create a complete project plan including technology recommendations, architecture overview, development phases, and risk assessment."
```

**Step 2: Technology Stack Selection**

```bash
"Based on the project plan, recommend the optimal technology stack considering:
- Development team size: [solo/small team/enterprise]
- Expected user scale: [hundreds/thousands/millions]
- Budget constraints: [startup/enterprise]
- Deployment preferences: [cloud/on-premise/hybrid]
- Maintenance requirements: [minimal/moderate/high]
Justify each technology choice with specific reasoning."
```

**Step 3: Project Scaffolding**

```bash
"Create a production-ready project structure for [project name] using [selected stack]:
- Proper folder organization
- Configuration files for all tools
- Development and production environment setup
- CI/CD pipeline configuration
- Documentation structure
- Security configurations
- Testing framework setup
Include all necessary config files, package.json, Docker configs, and README with setup instructions."
```

### **Template Creation Patterns**

**Frontend Template (Phased Approach):**

```bash
# Phase 1: Core Structure
"Create the basic React TypeScript project structure with:
- Vite build setup with TypeScript
- Folder organization for components, hooks, utils
- Basic routing with React Router
- Essential configuration files"

# Phase 2: Development Tooling
"Add development tooling:
- ESLint and Prettier configuration
- Husky pre-commit hooks
- VS Code workspace settings
- Testing setup with Vitest"

# Phase 3: UI Foundation
"Set up UI foundation:
- Tailwind CSS with configuration
- Component library structure
- Design token system
- Storybook for component development"

# Phase 4: State and API Integration
"Add state management and API integration:
- State management setup (Zustand/Redux)
- API client configuration
- Form handling with React Hook Form
- Error boundary implementation"
```

**Backend Template (Phased Approach):**

```bash
# Phase 1: Server Foundation
"Create Node.js API server foundation:
- Express/Fastify setup with TypeScript
- Basic middleware configuration
- Environment variable management
- Health check endpoint"

# Phase 2: Database Integration
"Add database layer:
- PostgreSQL connection setup
- Migration system configuration
- ORM setup (Prisma/TypeORM)
- Database seeding scripts"

# Phase 3: Authentication & Security
"Implement authentication and security:
- JWT authentication system
- Rate limiting middleware
- CORS configuration
- Input validation with Joi/Zod"

# Phase 4: Testing & Documentation
"Add testing and documentation:
- Jest test configuration
- API testing with supertest
- OpenAPI/Swagger documentation
- Logging with Winston"
```

### **Configuration Management**

**Environment Setup:**

```bash
"Create comprehensive environment configuration:
- .env templates for all environments
- Environment variable validation
- Docker environment handling
- CI/CD environment configuration
Include validation scripts and documentation."
```

**Development Tooling:**

```bash
"Set up integrated development tooling:
- Package manager configuration
- TypeScript strict configuration
- Linting rules for code quality
- Formatting with consistent rules
- Pre-commit hooks for quality gates
- Debug configuration for development"
```

---

## 🎯 Advanced Command Line Options

*CLI usage for power users*

### **Permission Management**

```bash
# Skip permissions (use with development branches only)
claude --dangerously-skip-permissions

# Controlled permissions
claude --allowedTools Edit,Bash(git:*,npm:*,test:*)

# Permission modes
claude --permission-mode ask      # Ask for each action (default)
claude --permission-mode plan     # Plan mode only, no execution
claude --permission-mode auto     # Auto-approve safe actions
```

### **Output Formatting**

```bash
claude --output-format text       # Plain text (default)
claude --output-format json       # Structured JSON output
claude --output-format stream-json # Streaming JSON for CI/CD
```

### **Model and Session Management**

```bash
claude --model sonnet            # Use only Sonnet
claude --model opus              # Use only Opus
claude --continue               # Continue most recent session
claude --resume session-id      # Resume specific session
claude --list-sessions          # Show available sessions
```

### **Debugging and Monitoring**

```bash
claude --verbose                 # Detailed output
claude --debug                   # Debug mode with tool traces
claude --log-file claude.log     # Log to file
claude --profile                 # Performance profiling
```

---

## 🔧 Troubleshooting & Performance

*Solutions for common issues and optimization strategies*

### **Common Issues and Solutions**

**Permission Fatigue:**

```bash
# Problem: Claude asks permission constantly
# Solution: Use development branch strategy
git checkout -b ai/feature-development
claude --dangerously-skip-permissions
```

**Context Window Problems:**

```bash
# Problem: Context window full, degraded performance
# Solutions:
/clear                    # Clear regularly
/compact focus:current-task # Compress conversations
/save current-work && /clear && /load current-work # Reset with context
```

**Model Selection Issues:**

```bash
# Use appropriate model for task complexity
claude --model opus -p "complex architectural decision"
claude --model sonnet -p "simple refactoring task"
```

### **Performance Optimization**

**Response Speed:**

1. Be specific in requests (reduces back-and-forth)
2. Use /clear frequently (smaller context)
3. Reference specific files (focused analysis)
4. Choose appropriate model for task complexity
5. Break complex tasks into smaller pieces

**Token Usage:**

```bash
/cost                    # Monitor usage
/compact                 # Compress when needed
claude -p "brief summary" # Request concise responses
```

### **Development Metrics**

```bash
"Generate development summary:
- Features completed this session
- Code quality improvements made
- Tests added or updated
- Performance optimizations implemented
- Documentation updates
Include metrics like lines of code, test coverage changes, and performance improvements."
```

---

## 🔌 MCP Integration

*External tool and service integration for enhanced workflows*

Model Context Protocol (MCP) allows Claude Code to integrate with external tools, databases, APIs, and services, dramatically expanding its capabilities beyond basic file editing.

### **What is MCP?**

MCP enables Claude Code to:

- Connect to databases (PostgreSQL, MySQL, MongoDB)
- Interact with cloud services (AWS, Azure, GCP)
- Access external APIs (GitHub, Slack, Jira)
- Use specialized tools (Docker, Kubernetes, monitoring systems)
- Read from data sources (logs, metrics, documentation)

### **Setting Up MCP Integration**

**Installation and Configuration:**

```bash
# Install MCP server for your desired integration
npm install -g @mcp/postgres-server
npm install -g @mcp/github-server
npm install -g @mcp/docker-server

# Configure MCP servers in ~/.claude/mcp_servers.json
{
  "postgres": {
    "command": "mcp-postgres-server",
    "args": ["--connection-string", "postgresql://user:pass@localhost:5432/db"]
  },
  "github": {
    "command": "mcp-github-server",
    "args": ["--token", "$GITHUB_TOKEN"]
  },
  "docker": {
    "command": "mcp-docker-server",
    "args": ["--socket", "/var/run/docker.sock"]
  }
}
```

**Enabling MCP in Claude Code:**

```bash
# Start Claude Code with MCP integration
claude --enable-mcp

# Or enable specific MCP servers
claude --mcp-servers postgres,github,docker
```

### **Database Integration Use Cases**

**Schema Analysis and Migration:**

```bash
"Connect to our PostgreSQL database and:
1. Analyze the current schema structure
2. Identify potential performance bottlenecks
3. Suggest indexes for slow queries
4. Generate migration scripts for schema improvements
5. Create data validation queries"
```

**Data-Driven Development:**

```bash
"Query the user_analytics table to understand:
- Most common user interaction patterns
- Performance bottlenecks in user flows
- Feature usage statistics
Then suggest code optimizations based on actual usage data."
```

**Database-Code Synchronization:**

```bash
"Compare the database schema with our TypeScript interfaces in @types/database.ts:
- Identify mismatches between DB and code
- Generate updated TypeScript types
- Create validation schemas that match DB constraints
- Suggest API endpoint improvements based on schema"
```

---

## 🤖 Subagents Integration

*Specialized AI assistant workflows for complex development tasks*

Subagents are specialized Claude instances that focus on specific domains, allowing you to delegate specialized tasks while maintaining context and coordination with your main development session.

### **Understanding Subagents**

Subagents enable:

- **Domain Expertise**: Specialized knowledge (security, performance, testing, documentation)
- **Parallel Processing**: Multiple focused tasks simultaneously  
- **Context Isolation**: Separate complex tasks without cluttering main session
- **Specialized Workflows**: Custom prompts and behaviors for specific tasks

### **Setting Up Subagents**

**Basic Subagent Creation:**

```bash
# Create specialized subagents for different domains
claude --create-subagent security-expert --context-file security-patterns.md
claude --create-subagent performance-analyst --context-file performance-benchmarks.md  
claude --create-subagent test-engineer --context-file testing-strategies.md
claude --create-subagent docs-writer --context-file documentation-standards.md
```

**Subagent Configuration Files:**

```bash
# ~/.claude/subagents/security-expert.json
{
  "name": "security-expert",
  "specialization": "application security and vulnerability analysis",
  "context_files": ["security-patterns.md", "OWASP-guidelines.md"],
  "default_instructions": "Always prioritize security in code analysis and suggestions",
  "tools": ["Edit", "Bash", "WebFetch"],
  "model": "opus"  // Use more powerful model for security analysis
}
```

### **Coordinated Multi-Subagent Workflows**

**Feature Development Pipeline:**

```bash
# Main session: Architecture and coordination
"Plan and coordinate development of payment processing system"

# Security subagent: Security analysis
claude --delegate security-expert "Design secure payment flow with PCI compliance"

# Performance subagent: Optimization
claude --delegate performance-analyst "Optimize payment processing for high throughput"  

# Testing subagent: Quality assurance
claude --delegate test-engineer "Create comprehensive test suite for payment system"

# Documentation subagent: Knowledge management
claude --delegate docs-writer "Create complete payment system documentation"
```

**Cross-Subagent Communication:**

```bash
# Subagents can share context through shared files
# Security subagent creates security-requirements.md
# Performance subagent reads requirements and creates optimized implementation
# Testing subagent validates both security and performance requirements

# Main session coordinates: 
"Integrate findings from all subagents into final implementation plan"
```

### **Subagent Management Commands**

```bash
# Subagent lifecycle management
claude --list-subagents                    # Show all subagents
claude --subagent-status security-expert   # Check subagent status
claude --kill-subagent test-engineer       # Stop specific subagent
claude --sync-subagents                    # Synchronize subagent contexts

# Communication with subagents
claude --query security-expert "What are the current security concerns?"
claude --broadcast "New deployment completed, update your contexts"
```

---

## 📚 Learning Mode

*Enhanced development with contextual guidance and educational insights*

Learning Mode transforms Claude Code into an interactive mentor that not only implements solutions but teaches you the underlying concepts, best practices, and reasoning behind every decision.

### **Activating Learning Mode**

```bash
# Enable learning mode for current session
/output-style learning

# Or start Claude Code in learning mode
claude --output-style learning

# Advanced learning mode with specific focus
claude --output-style learning --focus architecture,security,performance
```

### **How Learning Mode Works**

Learning Mode provides:

- **Conceptual Explanations**: Why specific approaches are chosen
- **Alternative Solutions**: Multiple ways to solve problems with trade-offs
- **Best Practices**: Industry standards and professional techniques
- **Common Pitfalls**: What to avoid and why
- **Progressive Learning**: Building complexity gradually
- **Interactive Q&A**: Follow-up questions to deepen understanding

### **Learning Mode Output Structure**

**Standard Implementation:**
```bash
# Regular mode output
"Created user authentication with JWT tokens and bcrypt password hashing."
```

**Learning Mode Output:**
```bash
# Learning mode provides educational context
"✅ IMPLEMENTATION: Created user authentication system

🎯 CONCEPT EXPLANATION:
JWT (JSON Web Tokens) provide stateless authentication by encoding user claims 
in a cryptographically signed token. This approach scales well because servers 
don't need to store session data.

🔐 SECURITY REASONING:
- bcrypt for password hashing: Adaptive hashing function designed to be slow
- Salt rounds set to 12: Balances security vs performance (2^12 iterations)
- JWT secret stored in environment: Prevents token forgery

⚖️ ALTERNATIVE APPROACHES:
1. Session-based auth: Better for highly sensitive apps, requires session storage
2. OAuth integration: Better for user experience, adds external dependency  
3. Passport.js: More features, higher complexity

⚠️ COMMON PITFALLS TO AVOID:
- Never store JWT secret in code (security vulnerability)
- Don't use symmetric encryption for passwords (use bcrypt, not md5/sha1)
- Implement token expiration (prevents indefinite access if compromised)

🔄 NEXT LEARNING STEPS:
- Implement refresh tokens for better security
- Add rate limiting to prevent brute force attacks
- Consider implementing 2FA for enhanced security

❓ FOLLOW-UP QUESTIONS:
- Would you like me to explain how JWT token validation works?
- Should we implement refresh token rotation for enhanced security?
- Want to learn about different password hashing algorithms?"
```

### **Domain-Specific Learning Focus**

**Architecture Learning:**

```bash
/output-style learning --focus architecture

"Implement a microservices communication pattern"

# Output includes:
# - Service architecture patterns (API Gateway, Event Sourcing, CQRS)
# - Communication patterns (Sync vs Async, Message Queues)
# - Data consistency patterns (Saga, 2PC)
# - Deployment and scaling considerations
# - Real-world examples and case studies
```

**Security Learning:**

```bash
/output-style learning --focus security  

"Add user input validation to the API"

# Output includes:
# - OWASP Top 10 vulnerabilities explained
# - Input validation techniques and libraries
# - SQL injection prevention methods
# - XSS protection strategies
# - Security testing approaches
# - Compliance considerations (GDPR, PCI-DSS)
```

**Performance Learning:**

```bash
/output-style learning --focus performance

"Optimize the database queries for the user dashboard"

# Output includes:
# - Query optimization techniques (indexes, query plans)
# - Caching strategies (Redis, memcached, CDN)
# - Database design patterns (normalization vs denormalization)
# - Performance monitoring and metrics
# - Load testing methodologies  
# - Scalability patterns
```

### **Interactive Learning Workflows**

**Concept Deep-Dive Sessions:**

```bash
/output-style learning

"Explain and implement a complete CI/CD pipeline"

# Learning mode creates structured curriculum:
# 1. Version Control Best Practices
# 2. Automated Testing Strategies  
# 3. Build and Deployment Automation
# 4. Infrastructure as Code
# 5. Monitoring and Observability
# 6. Security in CI/CD
# Each section includes theory, implementation, and hands-on exercises
```

**Problem-Solution Learning:**

```bash
"Our application is slow under high load. Teach me how to diagnose and fix performance issues."

# Learning mode provides:
# 1. Performance profiling techniques
# 2. Bottleneck identification methods
# 3. Solution implementation with explanations
# 4. Performance testing validation
# 5. Ongoing monitoring setup
# 6. Prevention strategies for future issues
```

### **Learning Mode Customization**

**Skill Level Adaptation:**

```bash
# Beginner level - more explanation, simpler concepts
claude --output-style learning --level beginner

# Intermediate level - balanced explanation with practical focus  
claude --output-style learning --level intermediate

# Advanced level - deeper technical details, complex patterns
claude --output-style learning --level advanced

# Expert level - cutting-edge techniques, research-based approaches
claude --output-style learning --level expert
```

**Learning Path Tracking:**

```bash
# Track learning progress
/learning-progress show

# Learning objectives for current project
/learning-objectives set "Master microservices architecture, implement observability, learn Kubernetes deployment"

# Review learned concepts
/learning-review architecture,performance

# Generate personalized learning recommendations
/learning-recommendations based-on-project
```

### **Educational Use Cases**

**Onboarding New Developers:**

```bash
# Create comprehensive onboarding experience
/output-style learning --focus fundamentals,project-specific

"Walk me through our entire codebase and explain the architecture decisions"

# Provides structured learning path through existing code
```

**Technology Migration Learning:**

```bash
# Learn while migrating
/output-style learning --focus migration

"Help me migrate from REST API to GraphQL while teaching me GraphQL concepts"

# Combines practical migration with comprehensive GraphQL education
```

**Best Practices Integration:**

```bash
# Learn industry standards while building
/output-style learning --focus best-practices

"Implement user authentication following industry best practices"

# Teaches security standards, code organization, testing practices
```

### **Learning Mode Commands**

```bash
/output-style learning                    # Enable learning mode
/output-style standard                    # Return to standard mode
/learning-focus add architecture          # Add learning focus area
/learning-focus remove security          # Remove focus area
/learning-level set intermediate         # Set learning level
/learning-save session-name              # Save learning session
/learning-export markdown                # Export learning content
```

---

## 📚 Resources

### **Official Documentation**

- [Claude Code Overview](https://docs.anthropic.com/en/docs/claude-code/overview) - Complete feature reference
- [CLI Reference](https://docs.anthropic.com/en/docs/claude-code/cli) - All command line options
- [MCP Integration](https://docs.anthropic.com/en/docs/claude-code/mcp) - External tool integration

---
