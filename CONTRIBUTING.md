# 🤝 Contributing to Real-Time Collaborative Workspace Platform

We love your input! We want to make contributing to this project as easy and transparent as possible, whether it's:

- Reporting a bug
- Discussing the current state of the code
- Submitting a fix
- Proposing new features
- Becoming a maintainer

## 🔄 Development Process

We use GitHub to host code, to track issues and feature requests, as well as accept pull requests.

### Branch Strategy

- `master`: Production-ready code
- `develop`: Integration branch for features
- `feature/*`: Feature development branches
- `hotfix/*`: Critical bug fixes
- `release/*`: Release preparation branches

### Workflow

1. Fork the repo and create your branch from `develop`
2. If you've added code that should be tested, add tests
3. If you've changed APIs, update the documentation
4. Ensure the test suite passes
5. Make sure your code lints
6. Issue that pull request!

## 📝 Pull Request Process

1. **Create a feature branch** from `develop`:
   ```bash
   git checkout develop
   git pull origin develop
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes** following our coding standards

3. **Write or update tests** for your changes

4. **Run the test suite** to ensure everything works:
   ```bash
   # Frontend tests
   cd frontend && npm test
   
   # Backend tests
   cd backend && mvn test
   ```

5. **Lint your code**:
   ```bash
   # Frontend
   cd frontend && npm run lint
   
   # Backend
   cd backend && mvn spotless:apply
   ```

6. **Commit your changes** using conventional commits:
   ```bash
   git add .
   git commit -m "feat: add real-time notifications"
   ```

7. **Push to your fork** and create a pull request:
   ```bash
   git push origin feature/your-feature-name
   ```

8. **Fill out the PR template** completely

9. **Request review** from at least 2 maintainers

## 📝 Commit Convention

We use [Conventional Commits](https://www.conventionalcommits.org/) for commit messages:

### Format
```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### Types
- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that do not affect the meaning of the code
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `perf`: A code change that improves performance
- `test`: Adding missing tests or correcting existing tests
- `chore`: Changes to the build process or auxiliary tools

### Examples
```bash
feat(auth): add JWT token refresh mechanism
fix(api): resolve GraphQL subscription memory leak
docs(readme): update installation instructions
test(workspace): add integration tests for workspace creation
chore(deps): upgrade Spring Boot to 3.2.1
```

## 🏗️ Coding Standards

### Frontend (React/TypeScript)

#### Code Style
- Use **TypeScript** for all new code
- Follow **ESLint** and **Prettier** configurations
- Use **functional components** with hooks
- Implement **proper error boundaries**
- Use **CSS Modules** or **styled-components**

#### Naming Conventions
- **Components**: PascalCase (`UserProfile.tsx`)
- **Hooks**: camelCase starting with "use" (`useUserData.ts`)
- **Utils**: camelCase (`formatDate.ts`)
- **Constants**: UPPER_SNAKE_CASE (`API_ENDPOINTS.ts`)

#### File Structure
```
src/
├── components/          # Reusable UI components
│   ├── common/          # Shared components
│   └── feature/         # Feature-specific components
├── hooks/              # Custom React hooks
├── services/           # API and external services
├── utils/              # Utility functions
├── types/              # TypeScript type definitions
├── graphql/            # GraphQL queries and mutations
└── assets/             # Static assets
```

### Backend (Spring Boot/Java)

#### Code Style
- Use **Java 17** features appropriately
- Follow **Google Java Style Guide**
- Use **Spotless** for code formatting
- Implement **proper exception handling**
- Use **Spring Boot best practices**

#### Architecture
- Follow **Clean Architecture** principles
- Use **GraphQL** for API design
- Implement **proper validation**
- Use **Spring Security** for authentication
- Implement **caching** where appropriate

#### Package Structure
```
com.rtcw/
├── application/        # Application services
├── domain/             # Domain entities and repositories
├── infrastructure/     # External concerns (DB, cache, etc.)
├── web/                # GraphQL resolvers and controllers
├── config/             # Configuration classes
└── security/           # Security configuration
```

## 🧪 Testing Standards

### Frontend Testing
- **Unit Tests**: Use Jest and React Testing Library
- **Integration Tests**: Test component interactions
- **E2E Tests**: Use Cypress for critical user journeys
- **Coverage**: Maintain >70% coverage

```javascript
// Example test structure
describe('UserProfile', () => {
  it('should display user information correctly', () => {
    // Test implementation
  });
  
  it('should handle loading states', () => {
    // Test implementation
  });
});
```

### Backend Testing
- **Unit Tests**: Use JUnit 5 and Mockito
- **Integration Tests**: Use Spring Boot Test
- **Repository Tests**: Use @DataJpaTest
- **GraphQL Tests**: Test resolvers and schema
- **Coverage**: Maintain >80% coverage

```java
@SpringBootTest
class UserServiceTest {
    
    @Test
    void shouldCreateUserSuccessfully() {
        // Test implementation
    }
    
    @Test
    void shouldThrowExceptionForInvalidData() {
        // Test implementation
    }
}
```

## 📚 Documentation

### Code Documentation
- **JSDoc** for TypeScript functions
- **Javadoc** for Java methods
- **README** updates for new features
- **API documentation** for GraphQL changes

### Examples
```typescript
/**
 * Formats a date according to the user's locale
 * @param date - The date to format
 * @param locale - The user's locale (defaults to 'en-US')
 * @returns Formatted date string
 */
function formatDate(date: Date, locale = 'en-US'): string {
  return date.toLocaleDateString(locale);
}
```

```java
/**
 * Creates a new workspace for the given user
 * @param userId The ID of the user creating the workspace
 * @param createRequest The workspace creation request
 * @return The created workspace
 * @throws UserNotFoundException if the user doesn't exist
 */
public Workspace createWorkspace(Long userId, CreateWorkspaceRequest createRequest) {
    // Implementation
}
```

## 📈 Performance Guidelines

### Frontend Performance
- Use **React.memo** for expensive components
- Implement **lazy loading** for routes
- Optimize **bundle size** with code splitting
- Use **Apollo Client** caching effectively
- Implement **virtualization** for large lists

### Backend Performance
- Use **database indexes** appropriately
- Implement **caching** with Redis
- Optimize **GraphQL** queries (avoid N+1)
- Use **async processing** for heavy operations
- Monitor **query performance**

## 🛡️ Security Guidelines

### Frontend Security
- **Validate** all user inputs
- **Sanitize** data before display
- Use **HTTPS** only
- Implement **CSP** headers
- Store **tokens securely**

### Backend Security
- **Validate** all inputs at the boundary
- Use **parameterized queries**
- Implement **rate limiting**
- **Audit** sensitive operations
- Follow **OWASP** guidelines

## 🐛 Bug Reports

We use GitHub issues to track public bugs. Report a bug by [opening a new issue](https://github.com/bhanu-1902/real-time-collaborative-workspace/issues/new?template=bug_report.md).

**Great bug reports** tend to have:

- A quick summary and/or background
- Steps to reproduce
- What you expected would happen
- What actually happens
- Notes (possibly including why you think this might be happening)

## ✨ Feature Requests

We use GitHub issues to track feature requests. Request a feature by [opening a new issue](https://github.com/bhanu-1902/real-time-collaborative-workspace/issues/new?template=feature_request.md).

## 📋 Code Review Process

### For Contributors
1. Ensure all tests pass
2. Update documentation
3. Follow the PR template
4. Respond to review feedback promptly
5. Keep PRs focused and atomic

### For Reviewers
1. Review within 48 hours
2. Be constructive and specific
3. Check for:
   - Code quality and standards
   - Test coverage
   - Performance implications
   - Security considerations
   - Documentation updates

## 🎆 Release Process

1. **Feature Complete**: All features for the release are merged to `develop`
2. **Create Release Branch**: `release/v1.x.x` from `develop`
3. **Testing**: QA testing and bug fixes
4. **Documentation**: Update changelog and version
5. **Merge**: Release branch to `master`
6. **Tag**: Create git tag for the release
7. **Deploy**: Automated deployment to production
8. **Backport**: Merge `master` back to `develop`

## 🎯 Quality Gates

Before merging, ensure:

- [ ] All tests pass (unit, integration, e2e)
- [ ] Code coverage thresholds met
- [ ] Linting passes
- [ ] Security scan passes
- [ ] Performance benchmarks met
- [ ] Documentation updated
- [ ] 2+ approvals from maintainers

## 📦 Environment Setup

### Prerequisites
- Node.js 18+
- Java 17+
- Maven 3.8+
- Docker & Docker Compose
- Git

### Quick Setup
```bash
# Clone the repository
git clone https://github.com/bhanu-1902/real-time-collaborative-workspace.git
cd real-time-collaborative-workspace

# Start development environment
docker-compose up -d

# Install frontend dependencies
cd frontend && npm install

# Install backend dependencies
cd ../backend && mvn clean install

# Run tests
npm test && mvn test
```

## 📞 Getting Help

- **Documentation**: Check the [docs](docs/) folder
- **Issues**: Search existing issues before creating new ones
- **Discussions**: Use GitHub Discussions for questions
- **Email**: Contact maintainers for sensitive issues

## 📄 License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

**Thank you for contributing to Real-Time Collaborative Workspace Platform!** 🚀