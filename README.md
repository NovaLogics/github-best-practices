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
  *Example:*   `feat(auth): Add password recovery option`

<br>

- **fix** : Fixes a bug    
  *Example:* `fix(cart): Correct item count calculation`

<br>

**Other Types**:
- **build** : Changes related to build tools or dependencies.
- **chore** : Routine tasks or changes that do not affect production code.
- **ci** : Changes related to continuous integration configurations.
- **docs** : Documentation changes.
- **style** : Code style changes (e.g., formatting, no functional changes).
- **refactor** : Code restructuring without changing behavior.
- **perf** : Performance improvements.
- **test** : Adding or modifying tests.
- **config** : Configuration changes.

<br>

## 2.4 Scope (Optional)
The scope provides additional context about which part of the code was modified. It should be placed in parentheses after the type.  
  *Example:*
  - `feat(ui): Improve button design`
  - `feat(api): Add new user endpoint`

<br>

### Examples : Type + Scope + Description

1. **feature** &nbsp; : &nbsp; `feat(ui): Add dark mode support`

2. **bugfix** &nbsp; &nbsp; : &nbsp;  `fix(user-profile): Resolve issue with profile image upload`

3. **hotfix** &nbsp; &nbsp; : &nbsp;  `hotfix(payment): Fix crash in payment gateway integration`

4. **release** &nbsp; : &nbsp;  `release(v2.1.0): Prepare release notes for version 2.1.0`

5. **chore** &nbsp; &nbsp; : &nbsp; &nbsp; `chore(deps): Update project dependencies to latest versions`

6. **test** &nbsp; &nbsp; : &emsp; `test(api): Add unit tests for user authentication`

7. **docs** &nbsp; &nbsp; : &nbsp; &nbsp;  `docs(contributing): Clarify contribution guidelines`

8. **refactor** : &nbsp;  `refactor(nav): Simplify navigation logic and remove unused code`

9.  **ci** &emsp; &emsp; : &emsp; `ci(actions): Update CI workflow for test coverage reporting`

10. **style** &nbsp; &nbsp; : &emsp; `style(button): Improve button alignment and spacing`

11. **perf** &nbsp; &nbsp; : &emsp; `perf(images): Optimize image loading for faster page rendering`

12. **config** &nbsp; : &nbsp;   `config(linter): Add new ESLint rules for better code consistency`

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

<br>

## 2.6 Footer and Breaking Changes

- **Footer** :  
  Used for additional information, like reviewers or references.  
  *Example :* `Reviewed-by: Bob <bob@example.com>`

- **Breaking Changes** :   
  Use the keyword "BREAKING CHANGE" if the commit introduces a significant change that may break backward compatibility. Breaking changes can be indicated:
  - In the subject by adding a `!` after the type/scope:
    - *Example :* `feat!: remove deprecated API methods`
  - In the footer:
    - *Example :*  `BREAKING CHANGE: Removed deprecated API methods`

<br>

*Full Example :*

  ```sql
  feat(auth)!: update user authentication method

  This commit changes the user authentication flow to enhance security by requiring multi-factor authentication.

  BREAKING CHANGE: The old session handling methods are removed.
  Update any references to the previous API.

  Reviewed-by: Alice <alice@example.com>
  ```

<br>

## 2.7  Why Use Conventional Commits

`Commit Messages` are general descriptions of changes made in a commit, often inconsistent due to a lack of rules. In contrast, `Conventional Commits` provide a standardized format (e.g., <type>([scope]): <description>) that enhances automation, clarity, and consistency in commit messaging.

Following the **Conventional Commits** specification ensures a clear and consistent commit history, which makes it easier to:

- **Automatically Generate Changelogs**: Tools can generate changelogs based on commit messages.
- **Semantic Versioning**: Determine version bumps based on the type of changes (patch, minor, or major).
- **Communicate Changes Clearly**: Teams and contributors can understand the nature of changes from the commit history.
- **Automate Processes**: Trigger builds, tests, and deployments based on the type of commits.
- **Encourage Collaboration**: Commit standards make it easier for new contributors to understand and participate in the project.



<br>

<hr>
<div align="center">

<kbd>[&nbsp; ⮝ &nbsp;  BACK TO TOP  &nbsp;&nbsp;&nbsp;](#contents) </kbd>
</div>
<hr>

<br>

<br>