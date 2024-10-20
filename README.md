<h1 align="center" >  
GitSafe: Best Practices for GitHub
</h1>

<br>

Hey developers! Here are some quick tips to help you use Git better. You probably already know Git, the tool that keeps your code safe and makes collaboration easier. Have you ever created a branch and forgotten why? Or struggled to understand a commit from the file changes? If so, these tips are for you!


### Why follow Git standards?

- **Improves Clarity**: Organized code is easier to read.
- **Enhances Team Collaboration**: Consistent guidelines facilitate teamwork.
- **Simplifies Project Structure**: Aids in quickly locating files and understanding setups.
- **Better Documentation**: Clearly tracks changes for easier contributions.
- **Boosts Code Quality**: Consistency results in cleaner code.
- **Automatic Changelogs**: Standards help generate changelogs automatically.
- **Streamlines CI/CD**: Improves efficiency in continuous integration and deployment processes.

<br>



# Contents

1. [Branch Naming Conventions ->](#1-branch-naming-conventions)
2. [Commit Message Guidelines & Conventional Commits ->](#2-commit-message-guidelines--conventional-commits)

<br>

<hr>

<br>


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
  Use only  
  🗸 lowercase letters ( a-z ),  
  🗸 numbers ( 0-9 ),  
  🗸 hyphens ( - )  
  in branch names.  
  Try to avoid punctuation, spaces, underscores, or special characters whenever possible.

- **Avoid Unnecessary Hyphens**   
  Don’t add extra or trailing hyphens, like in `feat/new—cart-`

- **Short and Clear**  
  Keep branch names brief but descriptive enough to quickly convey their purpose.


<br>


## 1.2 Understanding Branch Prefixes

Using prefixes for branches helps categorize them by their function, enhancing clarity and facilitating automated processes. Here are some commonly used branch type prefixes:

#### Most Common Branch Prefixes

These prefixes are frequently used in projects to categorize branches clearly:

- **feature/**   
  For new features or enhancements  [ `feature/` or `feat/` ]  
  *examples:*   
  - `feature/user-authentication`
  - `feature/payment-integration`
  - `feature/blog-posts`

<br>

- **bugfix/**    
  For fixing bugs    [ `bugfix/ `or `fix/` ]  
  *examples:*   
  - `bugfix/navbar-color-issue`
  - `bugfix/cart-quantity-update`
  - `bugfix/login-error-message`

<br> 

- **hotfix/**    
  For urgent fixes, often in production    
  *examples:*   
  - `hotfix/fix-crash-on-launch`
  - `hotfix/urgent-payment-bug`
  - `hotfix/critical-login-bug`

<br> 

- **release/**    
  For preparing release versions     
  *examples:*  
  - `release/v1.0.0`
  - `release/v2.3.1-beta`
  - `release/v3.0.0-final`

 <br> 

- **chore/**   
  For small maintenance tasks, such as refactoring or updating dependencies     
  *examples:*  
  - `chore/update-dependencies`
  - `chore/cleanup-unused-code`
  - `chore/upgrade-npm-packages`
  - `chore/refactor-project-structure`

<br> 
  
- **test/**   
    For adding or updating tests     
  *examples:*  
  - `test/add-user-auth-tests`
  - `test/update-product-tests`
  - `test/improve-checkout-test-coverage`
  - `test/fix-login-page-tests`

<br> 
  
- **docs/**   
  For documentation updates     
  *examples:*  
  - `docs/update-api-docs`
  - `docs/improve-readme`
  - `docs/add-contributing-guidelines`
  - `docs/architecture-overview`
  
<br> 

- **refactor/**   
  For code refactoring without changing functionality     
  *examples:*  
  - `refactor/improve-code-structure`
  - `refactor/optimize-query-performance`
  - `refactor/cleanup-css-styles`
  - `refactor/remove-deprecated-methods`

<br> 

- **ci/**    
  For *Continuous Integration or Deployment* related changes    
  *examples:* 
  - `ci/add-docker-support`
  - `ci/improve-ci-pipeline`
  - `ci/fix-automated-tests`
  - `ci/update-github-actions`

<br> 

- **style/**     
  For code style changes    
  *examples:* 
  - `style/improve-css-indentation`
  - `style/update-linter-rules`
  - `style/clean-up-html-structure`
  - `style/refactor-component-styles`
  
<br> 

- **perf/**     
  For performance improvements     
  *examples:*  
  - `perf/improve-load-time`
  
<br> 

- **config/**    
    For configuration file changes     
  *examples:*  
  - `config/update-webpack`

<br>


## 1.3 Incorporating Ticket Numbers

When your project utilizes an issue tracking tool such as Jira or GitHub Issues, it's helpful to add the issue identifier to the branch name for straightforward tracking.

For instance: `bugfix/proj-456-fix-user-login-issue`


<br>

<hr>
<div align="center">

<kbd>[&nbsp; ⮝ &nbsp;  BACK TO TOP  &nbsp;&nbsp;&nbsp;](#contents) </kbd>
</div>
<hr>

<br>

<br>

# 2. Commit Message Guidelines & Conventional Commits

This document provides a set of rules and best practices for writing clear, structured commit messages. 
It is based on the **Conventional Commits** specification, which aligns with **Semantic Versioning (SemVer)** and helps maintain an easy to follow commit history.

## 2.1 Structure of a Commit Message

A well-structured commit message is made up of the following elements:

- `<type>([optional scope]): <short description>` - This is the subject
- `[optional body]` - Extra details about the changes (if needed)
- `[optional footer]` - Additional information (if needed)

<br>

#

- **Type**: Indicates the kind of change made.
- **Scope (Optional)**: Adds extra context about which part of the project was affected.
- **Description**: A brief explanation of what was changed (start with a capital letter).
- **Body (Optional)**: Detailed information, if necessary. Leave a blank line between the description and body.
- **Footer (Optional)**: Additional information such as breaking changes or who reviewed the code.

<br>


## 2.2 Message Subject Guidelines

- **Use Command Form**  
  Write the message like a command. Begin with an action word (verb). 

  *Example:*  
  Use `fix: Resolve login issue`  🗸  
  instead of `fix: Resolved login issue` ⓧ
  
- **Keep It Short**  
  Limit the subject line to 50 characters.  
  This helps make the message easy to read in tools like `git log --oneline`. Avoid adding unnecessary words or symbols, and don’t end with a period.
  
- **Start with a Capital Letter**  
  The first word of the subject should always be capitalized.


<br>


## 2.3 Common Types of Commits

Add a type before the subject to show what kind of change it is.  
**Common types are**:

- **feat** : Introduces a new feature to the codebase   
  *Example:*  
  - `feat(auth): Add password recovery option`
  - `feat(ui): Add dark mode support`

<br>

- **fix** : Fixes a bug    
  *Example:*
  - `fix(cart): Correct item count calculation`
  - `fix(user-profile): Resolve issue with profile image upload`

<br>

**Other Types**:
- **build** : Changes related to build tools or dependencies.
  - `build(webpack): Upgrade webpack to version 5 for faster builds`
<br>

- **chore** : Routine tasks or changes that do not affect production code.
  - `chore(deps): Update project dependencies to latest versions`
  
<br>

- **ci** : Changes related to continuous integration configurations.
  - `ci(actions): Update CI workflow for test coverage reporting`
  
<br>

- **docs** : Documentation changes.
  - `docs(contributing): Clarify contribution guidelines` 
  
<br>

- **style** : Code style changes (e.g., formatting, no functional changes).
  - `style(button): Improve button alignment and spacing`
  
<br>

- **refactor** : Code restructuring without changing behavior.
  - `refactor(nav): Simplify navigation logic and remove unused code`
  
<br>

- **perf** : Performance improvements.
   - `perf(images): Optimize image loading for faster page rendering` 

<br>

- **test** : Adding or modifying tests.
  - `test(api): Add unit tests for user authentication`
  
<br>

- **config** : Configuration changes.
  - `config(linter): Add new ESLint rules for better code consistency`
  
- **hotfix**:
   - `hotfix(payment): Fix crash in payment gateway integration`

- **release**:
   - `release(v2.1.0): Prepare release notes for version 2.1.0`

<br>

## 2.4 Scope (Optional)
The scope provides additional context about which part of the code was modified. It should be placed in parentheses after the type.  
  *Example:*
  - `feat(ui): Improve button design`
  - `feat(api): Add new user endpoint`

 <br>

## 2.5 Message Body Guidelines
  
- Leave a blank line between the subject and the body.
- Use the body for detailed explanations, especially for complex changes.
- Keep each line in the body under 72 characters.
- If necessary, use multiple paragraphs to explain what, why, and how changes were made.  
  
  *Example:*

  ```scss
  fix(auth): Fix token validation error

  This commit corrects the logic for token validation, ensuring that expired tokens are properly rejected. This improves security by preventing unauthorized access.
  ```
---

## Footer and Extra Information:
- **Footer**: Include more information, such as who reviewed the code.  
  Example: `Reviewed-by: Bob <bob@example.com>`

- **Breaking Changes**: Use “BREAKING CHANGE” when the commit introduces a major change that could break something.  
  Example: `build!: migrate to webpack 5`  
  Or, explain in the footer:  
  `BREAKING CHANGE: Drop support for webpack 4 configurations.`

- **Multi-Paragraph Body**: For complex commits, you can use more than one paragraph to explain what, why, and how changes were made.

---