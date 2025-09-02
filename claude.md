# SaaS Development Context

## Development Philosophy

**Project Type:** Solo developer building SaaS products  
**Mission:** Ship fast, learn fast, iterate based on user feedback  
**Core Principle:** User value over perfect code  

## Solo Developer Constraints

- **Time Pressure:** Build features that users want, optimize for development velocity
- **Maintenance Reality:** Code must be debuggable at 3 AM when users report issues
- **Learning Focus:** Understand *why* patterns work, not just *what* to implement
- **Scale Preparation:** Anticipate team growth without over-engineering current needs
- **Resource Limits:** Optimize for cost-effective infrastructure and minimal operational overhead

## SaaS Business Context

**Stage:** Early-stage to growth SaaS (MVP → Product-Market Fit → Scale)  
**Focus:** User acquisition, retention, and revenue growth  
**Success Metrics:** User engagement, conversion rates, revenue per user, churn reduction  
**Growth Strategy:** Organic acquisition (SEO, AI discovery) + product-led growth  

### Business Priorities (in order):

1. **User-Impacting Issues:** Bugs that block signups, payments, or core feature usage
2. **Revenue Protection:** Systems that prevent lost customers or failed transactions
3. **Growth Enablers:** Features and optimizations that drive user acquisition and retention
4. **Technical Debt:** Refactoring that improves development velocity without user impact

## Technical Stack Philosophy

**Choose Boring Technology:** Proven, maintainable solutions over cutting-edge complexity  
**Performance Matters:** Fast user experiences drive better conversion and retention  
**Security First:** User trust is fundamental to SaaS success  
**Type Safety:** Catch bugs before users see them  
**Test Critical Paths:** Focus on user journeys that affect revenue and retention  

### Technology Decision Framework:

- **Maintainable by one person** under feature development pressure
- **Scales with user growth** without architectural rewrites
- **Debuggable in production** with clear error messages and logging
- **Cost-effective** for startup budgets and resource constraints
- **User-focused** optimizing for experience over technical elegance

## Development Workflow

### Daily Development:

1. **User Impact First:** Prioritize features and fixes by user value
2. **Quality Gates:** Automated checks (Biome, tests) preventing regressions
3. **Fast Feedback:** Development tools optimized for quick iteration cycles
4. **Documentation:** Write code that future-you will understand

### Feature Development Process:

1. **User Problem:** Start with real user need or pain point
2. **Simple Solution:** Build minimal viable implementation
3. **Quality Assurance:** Test critical user paths
4. **Performance Check:** Ensure acceptable user experience
5. **Security Review:** Protect user data and business operations
6. **Ship Fast:** Deploy with confidence, monitor, iterate

## SaaS-Specific Considerations

### User Experience:

- **Performance Budget:** < 3s page loads, responsive interactions
- **Accessibility:** WCAG compliance for broader user reach
- **Mobile-First:** Design for mobile users, enhance for desktop
- **Error Handling:** Graceful failures that don't confuse users

### Business Operations:

- **Multi-Tenancy:** User data isolation and security
- **Billing Integration:** Seamless payment flows and subscription management
- **User Onboarding:** Minimize friction in signup and first-value experiences
- **Analytics:** Track user behavior and business metrics for growth decisions

### Security Requirements:

- **User Data Protection:** GDPR compliance and privacy-first design
- **Authentication:** Secure user sessions and access control
- **Payment Security:** PCI compliance and secure transaction handling
- **Vulnerability Management:** Regular security updates and monitoring

## Learning Objectives

### Technical Skills

- **Full-Stack Development:** Frontend to backend to deployment
- **Performance Optimization:** User-perceived speed and system efficiency
- **Security Awareness:** Protect users and business from common threats
- **Quality Automation:** Tools and processes that catch issues early

### Business Skills

- **User-Focused Development:** Connect technical decisions to business outcomes
- **Growth Engineering:** Technical implementations that drive user acquisition
- **Revenue Engineering:** Reliable systems that protect and grow revenue
- **Scalability Planning:** Architecture that grows with business success

## Collaboration with Mentors

### When Working with Any Mentor

- **Start with Context:** Mentor will analyze your specific situation first
- **Learn Through Building:** Understand concepts through practical implementation
- **Ask Questions:** Challenge assumptions and explore trade-offs
- **Focus on User Impact:** Connect all technical decisions to user and business outcomes
- **Plan for Growth:** Consider how solutions evolve as your SaaS scales

### Expected Learning Outcomes

- **Sustainable Patterns:** Code and architecture that remains maintainable as you grow
- **Business Understanding:** Technical skills that directly support SaaS success
- **Problem-Solving Skills:** Systematic approaches to debugging and optimization
- **Growth Preparation:** Foundations that support team scaling and feature expansion

## Current Project Context

*[Update this section with specific information about your current SaaS project]*

**Product:** [Brief description of your SaaS]  
**Users:** [Target audience and current user base]  
**Stage:** [MVP, Growth, Scaling]  
**Technical Challenges:** [Current biggest technical priorities]  
**Business Goals:** [Key metrics you're optimizing for]  

### Technology Stack

**Programming Languages:**

- Primary: [e.g., TypeScript, Python, Go]
- Secondary: [e.g., SQL, Shell scripting]

**Frontend Stack:**

- Framework: [e.g., React, Next.js]
- Styling: [e.g., Tailwind CSS]
- Component Library: [e.g., Storybook]
- State Management: [e.g., Zustand, Redux]

**Backend Stack:**

- Framework: [e.g., Fastify, Chi, Django]
- Database: [e.g., PostgreSQL via Supabase, MySQL]
- ORM/Query Builder: [e.g., Drizzle, Prisma]
- Caching: [e.g., Redis, Memcached]
- Authentication: [e.g., Clerk, Auth0, custom JWT]

**Infrastructure & DevOps:**

- Containerization: [e.g., Docker]
- CI/CD: [e.g., GitHub Actions, GitLab CI]
- Hosting: [e.g., Vercel, Railway, AWS]
- Monitoring: [e.g., Sentry, LogRocket]

**Business Tools:**

- Payments: [e.g., Stripe, PayPal]
- Analytics: [e.g., PostHog, Mixpanel]
- Email: [e.g., Resend, SendGrid]
- Communication: [e.g., Discord, Slack integrations]

**Development Tools:**

- Code Quality: [e.g., Biome, ESLint, Prettier]
- Testing: [e.g., Playwright, Jest, Vitest]
- Version Control: [e.g., Git with GitHub/GitLab]
- Package Management: [e.g., pnpm, npm, yarn]

**Mobile (if applicable):**

- Platform: [e.g., React Native, Native iOS/Android]
- Deployment: [e.g., App Store, Google Play]  

---

*This context informs all mentor interactions. Each mentor will reference this shared understanding while providing domain-specific expertise and educational guidance.*
