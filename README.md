# GradientHQ Development Standards

This repository serves as the development standards hub for the GradientHQ organization, containing commit message conventions, workflow configurations, and other development standards to ensure code quality and consistency across all organizational repositories.

##  Standards Overview

###  Currently Configured Standards

- **Commit Message Convention** - Based on Conventional Commits standard
- **Automated Checks** - GitHub Actions workflows
- **Code Quality Assurance** - Unified linting and formatting rules

##  Repository Structure

```
.
├── .commitlintrc.json          # Commit message convention configuration
├── .github/
│   └── workflows/
│       └── commitlint.yml      # Automated commit message check workflow
└── README.md                   # This standards documentation
```

##  Commit Message Convention

### Convention Format

```
<type>: <short description>

[optional detailed description]

[optional footer]
```

### Supported Commit Types

| Type | Description | Example |
|------|-------------|---------|
| `feat` | New feature | `feat: add user login functionality` |
| `fix` | Bug fix | `fix: resolve login page styling issue` |
| `docs` | Documentation update | `docs: update API documentation` |
| `style` | Code formatting | `style: standardize code indentation` |
| `refactor` | Code refactoring | `refactor: restructure user service module` |
| `perf` | Performance optimization | `perf: optimize database query performance` |
| `test` | Test related | `test: add user module unit tests` |
| `chore` | Build/tool changes | `chore: update dependency versions` |

### Convention Requirements

- ✅ Title must not exceed 100 characters
- ✅ Use lowercase or sentence case
- ✅ Must use specified commit types
- ✅ Concisely describe the changes

### Commit Examples

**✅ Good commit message:**
```
feat: add user avatar upload functionality

Implement user avatar upload and preview features, supporting JPG and PNG formats,
with 2MB file size limit, including image compression and error handling.

Closes #123
```

**❌ Non-compliant commit message:**
```
update code
fixed some stuff
WIP
```

##  Automated Workflows

### Commitlint Check

- **Trigger**: Every Pull Request creation or update
- **Check Content**: Validates all commit messages against conventions
- **Runtime Environment**: Ubuntu + Node.js 20
- **Failure Handling**: Non-compliant PRs cannot be merged

##  Developer Guide

### 1. Local Development Setup

**Install commitlint (recommended):**
```bash
npm install --save-dev @commitlint/{config-conventional,cli}
```

**Configure Git Hook:**
```bash
npx husky add .husky/commit-msg 'npx --no -- commitlint --edit ${1}'
```

### 2. Daily Development Workflow

1. **Create feature branch**
   ```bash
   git checkout -b feat/new-feature
   ```

2. **Make standardized commits**
   ```bash
   git commit -m "feat: add new feature description"
   ```

3. **Create Pull Request**
   - Ensure commit messages comply with conventions
   - Wait for automated checks to pass
   - Request code review

### 3. Commit Message Best Practices

- **Use imperative mood**: "add" not "added"
- **Lowercase first letter**: unless it's a proper noun
- **Describe what changed**: explain what was done, not how
- **Link issues**: use `Closes #123` to link related issues

##  Standards Maintenance

### Modifying Standards

1. Create an Issue in this repository to discuss changes
2. Submit a Pull Request to modify configurations
3. After team review and approval, merge changes
4. New standards automatically apply to all repositories

### Standards Extension Roadmap

- [x] Code formatting standards (Prettier/ESLint)
- [ ] Branch naming conventions
- [ ] Pull Request templates
- [ ] Issue templates
- [ ] Code review guidelines

##  Getting Help

### Having Issues?

1. **Check documentation**: Review this README and related links first
2. **Search Issues**: Check if similar problems have been discussed
3. **Create Issue**: Describe specific problems and reproduction steps
4. **Contact team**: Seek help in team communication channels

### Have Improvement Suggestions?

1. Create an Issue in this repository
2. Provide detailed description of suggestions and rationale
3. Participate in discussions and solution refinement
4. Submit Pull Request to implement improvements

##  Related Resources

- [Conventional Commits Official Documentation](https://www.conventionalcommits.org/)
- [Commitlint Configuration Guide](https://commitlint.js.org/)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Git Best Practices](https://git-scm.com/book/en/v2)

## 📈 Standards Impact

Through unified development standards, we aim to achieve:

- ✅ **Improved Code Quality**: Unified standards and automated checks
- ✅ **Enhanced Collaboration**: Clear commit history and change records
- ✅ **Reduced Maintenance Costs**: Standardized code is easier to maintain
- ✅ **Faster Onboarding**: Clear development processes and standard documentation

---

**Important Notice**: Configurations in this repository affect all repositories in the GradientHQ organization. Please discuss thoroughly and test before making changes.

*Last Updated: 2025*
