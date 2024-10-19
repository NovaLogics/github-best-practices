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

## 1. Branch Naming Conventions

### 1.1 Fundamentals

## Essential Guidelines

- **Descriptive Names**  
  Use clear and specific names that show the branch's purpose right away. For example, choose `feature/shopping-cart` or `bugfix/header-overflow` instead of vague names.


- **Use Hyphens**  
  Separate words with hyphens (kebab case) for better readability. For instance, `bugfix/fix-login-issue` is easier to read than `bugfix/fixLoginIssue` or `bugfix/fix_login_issue`.

- **Lowercase Alphanumeric Characters**  
  Use only lowercase letters (a-z), numbers (0-9), and hyphens in branch names. Try to avoid punctuation, spaces, underscores, or special characters whenever possible.

- **Avoid Unnecessary Hyphens**   
  Don’t add extra or trailing hyphens, like in `feat/new—cart-`.

- **Short and Clear**  
  Keep branch names brief but descriptive enough to quickly convey their purpose.


