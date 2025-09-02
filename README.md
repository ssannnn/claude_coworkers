# Claude Code SaaS Development Mentors

A comprehensive collection of educational mentors designed for solo developers building SaaS products. Each mentor teaches domain expertise through practical implementation while maintaining focus on user value and business outcomes.

## 🎯 Philosophy

**Learn by Building** • **User Value First** • **Scale Smart** • **Ship Fast**

These mentors don't just complete tasks—they teach you sustainable patterns that grow with your SaaS. Every recommendation connects technical decisions to user experience and business outcomes.

## 🏗️ Complete Technology Stack Coverage

### 📚 **Language Foundations**

- **[javascript-mentor](agents/javascript-mentor.yaml)** - Modern JS patterns for SaaS development
- **[typescript-mentor](agents/typescript-mentor.yaml)** - Type safety and bug prevention
- **[python-mentor](agents/python-mentor.yaml)** - Backend language patterns
- **[golang-mentor](agents/golang-mentor.yaml)** - High-performance concurrent systems

### 🛡️ **Security & Authentication**

- **[owasp-security-mentor](agents/owasp-security-mentor.yaml)** - Application security essentials
- **[jwt-mentor](agents/jwt-mentor.yaml)** - Custom token-based authentication
- **[clerk-mentor](agents/clerk-mentor.yaml)** - Managed auth service with conversion optimization

### ⚙️ **Development Process**

- **[code-reviewer](agents/code-reviewer.yaml)** - Manual code review and quality standards
- **[biome-mentor](agents/biome-mentor.yaml)** - Automated code quality and formatting
- **[debugging-mentor](agents/debugging-mentor.yaml)** - Systematic problem-solving methodology
- **[github-actions-mentor](agents/github-actions-mentor.yaml)** - CI/CD and deployment automation

### 🏗️ **Frontend Development**

- **[react-mentor](agents/react-mentor.yaml)** - Component architecture and user interactions
- **[nextjs-mentor](agents/nextjs-mentor.yaml)** - Full-stack applications with SSR/SSG
- **[tailwind-mentor](agents/tailwind-mentor.yaml)** - Design systems and user experience
- **[storybook-mentor](agents/storybook-mentor.yaml)** - Component documentation and consistency
- **[astro-mentor](agents/astro-mentor.yaml)** - Ultra-fast marketing sites and content

### 🔧 **Backend Development**

- **[fastify-mentor](agents/fastify-mentor.yaml)** - High-performance Node.js APIs
- **[chi-mentor](agents/chi-mentor.yaml)** - Lightweight Go HTTP services

### 🗄️ **Data Layer**

- **[supabase-mentor](agents/supabase-mentor.yaml)** - Full-stack Postgres with real-time features
- **[drizzle-mentor](agents/drizzle-mentor.yaml)** - Type-safe ORM development
- **[redis-mentor](agents/redis-mentor.yaml)** - Caching and performance optimization

### 🚀 **Infrastructure & Deployment**

- **[docker-mentor](agents/docker-mentor.yaml)** - Containerization and reliable deployments
- **[playwright-mentor](agents/playwright-mentor.yaml)** - End-to-end testing and user journey protection

### 💰 **Business & Growth**

- **[stripe-mentor](agents/stripe-mentor.yaml)** - Payment systems and revenue collection
- **[seo-mentor](agents/seo-mentor.yaml)** - Search engine optimization for organic growth
- **[llo-mentor](agents/llo-mentor.yaml)** - LLM search optimization for AI-era discovery

### 📱 **Mobile Development**

- **[react-native-mentor](agents/react-native-mentor.yaml)** - Cross-platform mobile apps
- **[ios-mentor](agents/ios-mentor.yaml)** - Native iOS development with Swift/SwiftUI
- **[android-mentor](agents/android-mentor.yaml)** - Native Android development with Kotlin/Compose

## 🚀 Quick Start

### 1. Setup Your Project Context

Copy `claude.md` to your repository root and customize the **Current Project Context** section:

```markdown
## Current Project Context

**Product:** AI-powered project management SaaS for remote teams
**Users:** Remote team leads and project managers (0-500 users)
**Stage:** MVP - validating product-market fit
**Technical Challenges:** Real-time collaboration, user onboarding optimization
**Business Goals:** User activation rate, feature adoption, organic growth

### Technology Stack
**Programming Languages:**
- Primary: TypeScript, Python
- Secondary: SQL

**Frontend Stack:**
- Framework: Next.js 14 with App Router
- Styling: Tailwind CSS
- Component Library: Storybook
- State Management: Zustand

**Backend Stack:**
- Framework: Fastify
- Database: PostgreSQL via Supabase
- ORM: Drizzle
- Caching: Redis
- Authentication: Clerk
```

### 2. Copy Mentor Files

Create an `agents/` directory and copy your chosen mentor files:

```bash
mkdir agents
# Copy mentors you need from the artifacts above
```

### 3. Update Model Versions

Use the model update scripts when new Claude versions are released:

```bash
# Show current models across all agents
./scripts/update_models.sh

# Update to new model version
./scripts/update_models.sh -o claude-sonnet-4-20250514 -n claude-sonnet-4-20250601

# Dry run first to see what would change
./scripts/update_models.sh --dry-run -o old-model -n new-model
```

## 🎓 Usage Examples

### Basic Code Review

```bash
# Review recent changes with educational feedback
claude-code code-reviewer "Review the authentication middleware I just added"
```

### Feature Development

```bash
# Get React guidance for user onboarding
claude-code react-mentor "Help me build a user onboarding flow that reduces drop-off"

# Optimize API performance
claude-code fastify-mentor "This endpoint is slow under load, help me optimize it"
```

### Problem Solving

```bash
# Systematic debugging approach
claude-code debugging-mentor "Users report intermittent login failures, help me investigate"

# Performance optimization
claude-code redis-mentor "Help me implement caching for our user dashboard queries"
```

### Business Features

```bash
# Implement subscription billing
claude-code stripe-mentor "Help me add annual subscription upgrades to our billing flow"

# Improve search rankings
claude-code seo-mentor "Optimize our landing pages for 'project management software' keywords"
```

### Mobile Development

```bash
# Cross-platform mobile app
claude-code react-native-mentor "Help me add offline sync to our mobile app"

# Native iOS excellence
claude-code ios-mentor "Implement iOS-specific features like widgets and shortcuts"

# Native Android optimization
claude-code android-mentor "Optimize our app for Android's diverse device ecosystem"
```

## 🏛️ Architecture Strategies

### Full-Stack JavaScript/TypeScript

```
Frontend: Next.js + React + Tailwind + Storybook
Backend: Fastify + TypeScript
Database: Supabase + Drizzle
Mobile: React Native
```

**Best for:** Rapid development, code sharing, JavaScript expertise

### Performance-Optimized Stack

```
Frontend: Next.js + React + Tailwind
Backend: Go + Chi
Database: PostgreSQL + Redis
Mobile: Native iOS + Android
```

**Best for:** High-traffic applications, maximum performance

### Marketing-Focused Stack

```
SaaS App: Next.js full-stack
Marketing: Astro + SEO + LLO optimization
Mobile: React Native
```

**Best for:** Content marketing, organic growth, solo development

### Enterprise-Ready Stack

```
Frontend: Next.js + TypeScript + Storybook
Backend: Go + Chi (microservices)
Auth: Clerk (enterprise SSO)
Database: Supabase + Redis
DevOps: Docker + GitHub Actions
```

**Best for:** B2B SaaS, enterprise customers, team scaling

## 📚 Learning Pathways

### 👶 **Beginner Solo Developer**

1. **[javascript-mentor](agents/javascript-mentor.yaml)** → Learn language fundamentals
2. **[react-mentor](agents/react-mentor.yaml)** → Build user interfaces
3. **[nextjs-mentor](agents/nextjs-mentor.yaml)** → Create full-stack features
4. **[tailwind-mentor](agents/tailwind-mentor.yaml)** → Design consistent UIs
5. **[supabase-mentor](agents/supabase-mentor.yaml)** → Add database and auth

### 🚀 **Growing SaaS (Product-Market Fit)**

1. **[typescript-mentor](agents/typescript-mentor.yaml)** → Add type safety for refactoring confidence
2. **[stripe-mentor](agents/stripe-mentor.yaml)** → Implement revenue collection
3. **[playwright-mentor](agents/playwright-mentor.yaml)** → Protect critical user journeys
4. **[docker-mentor](agents/docker-mentor.yaml)** → Reliable deployment processes
5. **[seo-mentor](agents/seo-mentor.yaml)** → Organic user acquisition

### 📈 **Scaling SaaS (Growth Stage)**

1. **[biome-mentor](agents/biome-mentor.yaml) + [github-actions-mentor](agents/github-actions-mentor.yaml)** → Quality automation
2. **[redis-mentor](agents/redis-mentor.yaml)** → Performance optimization
3. **[storybook-mentor](agents/storybook-mentor.yaml)** → Design system scaling
4. **[react-native-mentor](agents/react-native-mentor.yaml)** → Mobile user engagement
5. **[owasp-security-mentor](agents/owasp-security-mentor.yaml)** → Enterprise security

### 🏢 **Enterprise SaaS**

1. **[golang-mentor](agents/golang-mentor.yaml) + [chi-mentor](agents/chi-mentor.yaml)** → High-performance backend
2. **[clerk-mentor](agents/clerk-mentor.yaml)** → Enterprise authentication (SSO, SCIM)
3. **[ios-mentor](agents/ios-mentor.yaml) + [android-mentor](agents/android-mentor.yaml)** → Platform-specific excellence
4. **[llo-mentor](agents/llo-mentor.yaml)** → AI-era discoverability

## 🛠️ Advanced Usage

### Combining Mentors

```bash
# Full-stack feature development
claude-code react-mentor "Plan the frontend for user team management"
claude-code fastify-mentor "Design the API endpoints for team operations"
claude-code supabase-mentor "Create the database schema for team hierarchies"

# Performance optimization
claude-code playwright-mentor "Test the performance impact of our changes"
claude-code redis-mentor "Cache frequently accessed team data"
```

### Technology Decisions

```bash
# Compare approaches
claude-code nextjs-mentor "When should I use SSR vs SSG for our SaaS pages?"
claude-code react-native-mentor "Compare React Native vs native development for our use case"

# Architecture reviews
claude-code debugging-mentor "Help me analyze this performance bottleneck systematically"
claude-code code-reviewer "Review our authentication architecture for security and maintainability"
```

## 📖 Educational Approach

Each mentor follows the same learning methodology:

### 🎯 **Context-Aware Teaching**

- Analyzes your specific SaaS and technology stack
- Connects technical decisions to business outcomes
- Adapts guidance to your development stage (MVP → Growth → Scale)

### 🧠 **Learning Through Building**

- Explains *what* and *why*, not just *how*
- Provides patterns that scale with your product
- Teaches debugging and problem-solving approaches

### 👥 **Solo Developer Focus**

- Acknowledges time and resource constraints
- Prioritizes maintainable patterns for one-person teams
- Prepares for future team scaling without over-engineering

### 📊 **Business-Driven Priorities**

1. **User-Impacting** → Fix what affects users immediately
2. **Business-Critical** → Protect revenue and growth
3. **Developer Velocity** → Speed up feature development
4. **Technical Debt** → Improve without breaking things

## 🔗 Key Resources

### Claude Code Documentation

- [Claude Code Overview](https://docs.anthropic.com/en/docs/claude-code) - Official documentation
- [Getting Started Guide](https://docs.anthropic.com/en/docs/claude-code/getting-started) - Setup and basic usage
- [Advanced Features](https://docs.anthropic.com/en/docs/claude-code/advanced-features) - Power user techniques

### Technology Documentation

- [Next.js Documentation](https://nextjs.org/docs) - Full-stack React framework
- [Fastify Documentation](https://fastify.dev/docs/latest/) - High-performance Node.js framework
- [Supabase Documentation](https://supabase.com/docs) - Open source Firebase alternative
- [Tailwind CSS Documentation](https://tailwindcss.com/docs) - Utility-first CSS framework
- [Stripe Documentation](https://stripe.com/docs) - Payment processing platform
- [React Native Documentation](https://reactnative.dev/docs/getting-started) - Cross-platform mobile development

### Best Practices & Patterns

- [SaaS Architecture Patterns](https://aws.amazon.com/saas/) - AWS SaaS best practices
- [Startup Engineering](https://lethain.com/staff-engineer/) - Scaling engineering organizations
- [TypeScript Best Practices](https://typescript-eslint.io/rules/) - Type-safe development patterns

<!-- ## 🤝 Contributing

This mentor collection grows with the SaaS development community:

1. **Fork** the repository
2. **Customize** mentors for your specific needs
3. **Share** improvements that benefit solo developers
4. **Submit** pull requests for new mentor domains

## 📄 License

MIT License - Build amazing SaaS products with confidence!

---

## 💡 Quick Tips

- **Start with context** - Update `claude.md` with your specific project details
- **Learn progressively** - Follow the learning pathways based on your stage
- **Combine mentors** - Use multiple mentors for complex features
- **Ask follow-ups** - Mentors love teaching through questions
- **Focus on users** - Every technical decision should improve user experience

Ready to build your SaaS with AI-powered mentorship? Pick a mentor and start learning! 🚀 -->
