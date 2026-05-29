# Contributing to Parent-Teacher Hub

Thank you for your interest in contributing to Parent-Teacher Hub! This document provides guidelines and instructions for contributing.

## Code of Conduct

- Be respectful and inclusive
- Welcome diversity and different perspectives
- Focus on constructive feedback
- Report unacceptable behavior to maintainers

## How to Contribute

### Reporting Bugs

1. Check existing issues to avoid duplicates
2. Use the bug report template
3. Include:
   - Clear description of the bug
   - Steps to reproduce
   - Expected behavior
   - Actual behavior
   - Screenshots if applicable
   - Environment details (OS, browser, versions)

### Suggesting Enhancements

1. Check existing issues and discussions
2. Use the feature request template
3. Describe the feature and its benefits
4. Provide use cases

### Pull Requests

#### Setup Development Environment

```bash
git clone https://github.com/Roba76/parent-teacher-hub.git
cd parent-teacher-hub
npm install
```

#### Create Feature Branch

```bash
git checkout -b feature/your-feature-name
```

Use naming conventions:
- `feature/description` - New features
- `bugfix/description` - Bug fixes
- `docs/description` - Documentation
- `refactor/description` - Code refactoring
- `test/description` - Testing improvements

#### Development Workflow

1. Make changes with clear, focused commits
2. Follow code style guidelines
3. Add/update tests
4. Update documentation
5. Run tests and linting locally

#### Commit Message Guidelines

```
type(scope): subject

body

footer
```

Examples:
- `feat(auth): add JWT token refresh`
- `fix(announcements): resolve notification bug`
- `docs(readme): update installation steps`
- `test(api): add endpoint tests`

#### Code Style

- Use ESLint and Prettier
- Follow TypeScript best practices
- Use meaningful variable names
- Add comments for complex logic
- Keep functions focused and small

#### Testing Requirements

- Write tests for new features
- Update tests for bug fixes
- Maintain >80% code coverage
- All tests must pass before PR submission

#### Submit Pull Request

1. Push branch to your fork
2. Open PR against `main` branch
3. Fill out PR template completely
4. Link related issues
5. Wait for review and CI checks

#### PR Review Process

- At least 2 approvals required
- All checks must pass
- Address reviewer feedback
- Keep PR updated with main branch

## Project Structure

See README.md for detailed project structure.

## Development Workflow

### Running the Application

**Docker (Recommended):**
```bash
docker-compose up
```

**Local:**
```bash
# Terminal 1: Frontend
cd frontend
npm run dev

# Terminal 2: Backend
cd backend
npm run dev
```

### Testing

```bash
# All tests
npm run test

# With coverage
npm run test:coverage

# Watch mode
npm run test:watch
```

### Linting

```bash
# Check
npm run lint

# Fix
npm run lint:fix
```

### Building

```bash
# Frontend
cd frontend
npm run build

# Backend
cd backend
npm run build
```

## Issue Labels

- `bug` - Something isn't working
- `enhancement` - New feature request
- `documentation` - Docs improvements
- `good first issue` - Good for newcomers
- `help wanted` - Need assistance
- `priority: high` - Urgent
- `priority: low` - Nice to have
- `in progress` - Someone is working on it
- `blocked` - Waiting on something else

## Release Process

1. Update version in package.json
2. Update CHANGELOG.md
3. Create release branch: `release/v1.0.0`
4. Merge to main and tag
5. Push release tag

## Questions or Need Help?

- Open an issue with `question` label
- Email: robgithubug@gmail.com
- Check existing discussions

## License

By contributing, you agree your contributions are licensed under the same license as the project.

Thank you for contributing! 🎉
