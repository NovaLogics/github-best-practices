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

- **`feature/`**   
  For new features or enhancements  [ feature/ or feat/ ]  
  *examples:*   
  - `feature/user-authentication`
  - `feature/payment-integration`
  - `feature/blog-posts`

<br>

- **`bugfix/`**    
  For fixing bugs    [ bugfix/ or fix/ ]  
  *examples:*   
  - `bugfix/navbar-color-issue`
  - `bugfix/cart-quantity-update`
  - `bugfix/login-error-message`


<br> 

- **`hotfix/`**    
  For urgent fixes, often in production    
  *examples:*   
  - `hotfix/fix-crash-on-launch`
  - `hotfix/urgent-payment-bug`
  - `hotfix/critical-login-bug`


<br> 

- **`release/`**    
  For preparing release versions     
  *examples:*  
  - `release/v1.0.0`
  - `release/v2.3.1-beta`
  - `release/v3.0.0-final`


 <br> 

- **`chore/`**   
  For small maintenance tasks, such as refactoring or updating dependencies     
  *examples:*  
  - `chore/update-dependencies`
  - `chore/cleanup-unused-code`
  - `chore/upgrade-npm-packages`
  - `chore/refactor-project-structure`

<br> 
  
- **`test/`**   
    For adding or updating tests     
  *examples:*  
  - `test/add-user-auth-tests`
  - `test/update-product-tests`
  - `test/improve-checkout-test-coverage`
  - `test/fix-login-page-tests`

  
<br> 
  
- **`docs/`**   
  For documentation updates     
  *examples:*  
  - `docs/update-api-docs`
  - `docs/improve-readme`
  - `docs/add-contributing-guidelines`
  - `docs/architecture-overview`
  
<br> 

#### Other Branch Prefixes  

These prefixes are used less frequently but still serve important purposes:

- **`refactor/`**   
  For code refactoring without changing functionality     
  *examples:*  
  - `refactor/improve-code-structure`
  - `refactor/optimize-query-performance`
  - `refactor/cleanup-css-styles`
  - `refactor/reorganize-component-files`
  - `refactor/remove-deprecated-methods`

<br> 

- **`ci/`**    
  For continuous integration or deployment-related changes    
  *examples:* 
  - `ci/setup-circleci`
  - `ci/improve-ci-pipeline`
  - `ci/fix-automated-tests`
  - `ci/add-docker-support`
  - `ci/update-github-actions`

<br> 

- **`style/`**     
  For code style changes    
  *examples:* 
  - `style/fix-code-formatting`
  - `style/improve-css-indentation`
  - `style/update-linter-rules`
  - `style/clean-up-html-structure`
  - `style/refactor-component-styles`
  
<br> 

- **`perf/`**     
  For performance improvements     
  *examples:*  
  - `perf/improve-load-time`
  
<br> 

- **`config/`**    
    For configuration file changes     
  *examples:*  
  - `config/update-webpack`


<br>

## 1.3 Incorporating Ticket Numbers

When your project utilizes an issue tracking tool such as Jira or GitHub Issues, it's helpful to add the issue identifier to the branch name for straightforward tracking.

For instance: `bugfix/proj-456-fix-user-login-issue`


<br>
<hr>