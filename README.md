<h1 align="center" >  
GitSafe: Best Practices for GitHub
</h1>

<br>

Hey developers! Here are some quick tips to help you use Git better. You probably already know Git, the tool that keeps your code safe and makes collaboration easier. Have you ever created a branch and forgotten why? Or struggled to understand a commit from the file changes? If so, these tips are for you!


### Why follow Git standards?

- **Improves Clarity**  
  Organized code is easier to read and understand.

- **Enhances Team Collaboration**  
  When everyone follows the same guidelines, it makes working together easier.

- **Simplifies Project Structure**  
  Helps you quickly find files and understand the project setup.

- **Better Documentation**  
  Tracks changes clearly, making it easy for others to follow and contribute.

- **Boosts Code Quality**  
  Consistent practices lead to cleaner, higher-quality code.

- **Automatic Changelogs**  
  Following standards helps generate changelogs without manual effort.

- **Streamlines CI/CD**  
  Makes your continuous integration (CI) and deployment (CD) processes more efficient.

<br>

<hr>

# 1. Branch Naming Conventions

## 1.1 Fundamentals

- **Descriptive Names**  
  Use clear and specific names that show the branch's purpose right away. For example, choose `feature/shopping-cart` or `bugfix/header-overflow` instead of vague names.


- **Use Hyphens**  
  Separate words with hyphens (kebab case) for better readability. 
  
  For instance, 🗸 `bugfix/fix-login-issue` is easier to read than   
  ⓧ `bugfix/fixLoginIssue` or   
  ⓧ `bugfix/fix_login_issue`

- **Lowercase Alphanumeric Characters**  
  Use only lowercase letters (a-z), numbers (0-9), and hyphens in branch names. Try to avoid punctuation, spaces, underscores, or special characters whenever possible.

- **Avoid Unnecessary Hyphens**   
  Don’t add extra or trailing hyphens, like in `feat/new—cart-`.

- **Short and Clear**  
  Keep branch names brief but descriptive enough to quickly convey their purpose.


<br>

## 1.2 Understanding Branch Prefixes

Using prefixes for branches helps categorize them by their function, enhancing clarity and facilitating automated processes. Here are some commonly used branch type prefixes:

#### Most Common Branch Prefixes

These prefixes are frequently used in projects to categorize branches clearly:

- **`feature/`**:  
  For new features or enhancements (e.g., `feature/shopping-cart`)

- **`bugfix/`**:  
    For fixing bugs (e.g., `bugfix/header-overflow`)

- **`hotfix/`**:  
  For urgent fixes, often in production (e.g., `hotfix/critical-bug-fix`)

- **`release/`**:  
    For preparing release versions (e.g., `release/v2.0`)
  
- **`chore/`**:  
  For small maintenance tasks, such as refactoring or updating dependencies (e.g., `chore/update-dependencies`)
  
- **`test/`**:  
    For adding or updating tests (e.g., `test/login-functionality`)
  
- **`docs/`**:  
  For documentation updates (e.g., `docs/api-guide`)

#### Other Branch Prefixes  

These prefixes are used less frequently but still serve important purposes:

- **`refactor/`**:  
  For code refactoring without changing functionality (e.g., `refactor/cart-logic`)

- **`ci/`**:  
  For continuous integration or deployment-related changes (e.g., `ci/update-ci-config`)

- **`style/`**:   
  For code style changes (e.g., `style/fix-indentation`)
  
- **`perf/`**:   
  For performance improvements (e.g., `perf/improve-load-time`)
  
- **`config/`**:   
    For configuration file changes (e.g., `config/update-webpack`)


<br>

## 1.3 Incorporating Ticket Numbers

When your project utilizes an issue tracking tool such as Jira or GitHub Issues, it's helpful to add the issue identifier to the branch name for straightforward tracking.

For instance: `bugfix/proj-456-fix-user-login-issue`


<br>

## 1.4 Recommended Branch Name Styles

#### Feature Branches
- `feature/user-authentication`
- `feature/shopping-cart`
- `feature/profile-settings`
- `feature/payment-integration`
- `feature/blog-posts`

#### Bugfix Branches
- `bugfix/navbar-color-issue`
- `bugfix/fix-product-image`
- `bugfix/cart-quantity-update`
- `bugfix/login-error-message`
- `bugfix/checkout-button-functionality`

#### Hotfix Branches
- `hotfix/urgent-payment-bug`
- `hotfix/fix-deployment-error`
- `hotfix/security-vulnerability-patch`
- `hotfix/critical-login-bug`
- `hotfix/fix-crash-on-launch`

#### Release Branches
- `release/v1.0.0`
- `release/v2.3.1`
- `release/v3.0.0-final`
- `release/v4.2.0-beta`
- `release/v5.1.0`

#### Chore Branches
- `chore/update-dependencies`
- `chore/cleanup-unused-code`
- `chore/optimize-build-process`
- `chore/upgrade-npm-packages`
- `chore/refactor-project-structure`

#### Test Branches
- `test/add-user-auth-tests`
- `test/update-product-tests`
- `test/improve-checkout-test-coverage`
- `test/fix-login-page-tests`
- `test/refactor-testing-framework`

#### Refactor Branches
- `refactor/improve-code-structure`
- `refactor/optimize-query-performance`
- `refactor/cleanup-css-styles`
- `refactor/reorganize-component-files`
- `refactor/remove-deprecated-methods`

#### Documentation Branches
- `docs/update-api-docs`
- `docs/improve-readme`
- `docs/add-contributing-guidelines`
- `docs/faq-section-update`
- `docs/architecture-overview`

#### Continuous Integration Branches
- `ci/setup-circleci`
- `ci/improve-ci-pipeline`
- `ci/fix-automated-tests`
- `ci/add-docker-support`
- `ci/update-github-actions`

#### Style Branches
- `style/fix-code-formatting`
- `style/improve-css-indentation`
- `style/update-linter-rules`
- `style/clean-up-html-structure`
- `style/refactor-component-styles`

