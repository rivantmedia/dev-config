# Coding Guidelines for Rivant Media Developers

This document is is currently a work in progress, and presents practical
guidelines for developers and others at Rivant Media who write or contribute to
code or repo. The guidelines cover:

- the use of Git and GitHub in large and small projects,
- coding style and documentation, and
- code reviews.

This is a reference document, and as such you are expected to dip into
it to read the parts that you need to know something about.

- If you write code outside of the Rivant Media developers' team, you should read the full text of
  this document at least once, but there is no expectation that you will
  remember it all.
- If you are a member of the Rivant Media developers' team, you should
  make yourself familiar with these guidelines.
- In any case, these are _guidelines_, not hard rules. We do not force
  these guidelines on you or on ourselves. We do however think that they
  would help to streamline our workflow, improve teamwork and benefit both
  ourselves individually as well as the "products" that we produce as
  developers.

Remember, these guidelines are supposed to make everything we produce
better, so that we can say _"I was a part of that!"_.

## Table of Contents

- [Coding Guidelines for NBIS Developers](#coding-guidelines-for-rivant-media-developers)
  - [Things to be aware of when writing code](#things-to-be-aware-of-when-writing-code)
    - [Intent](#intent)
    - [Comments in code](#comments-in-code)
    - [Readability](#readability)
    - [Best programming practices](#best-programming-practices)
    - [What programming language to use](#what-programming-language-to-use)
    - [Sensitive data](#sensitive-data)
  - [How to use Git and Github](#how-to-use-git-and-github)
  - [Guidelines for the Pull Request](#guidelines-for-the-pull-request)

## Things to be aware of when writing code

### Intent

Names of variable, functions, methods etc. should be clear and
descriptive, not cryptic. For example, function names might be a
verb or a question: `getGeneName()`, `findDownstreamFeature()`,
`isCircular()`, or `hasMultipleFlurbs()`.

It is common practice to name simple loop variables `i`, `j`, and `k`,
so there's no need to give them silly names like `theIndex` unless
it's necessary for some reason or other. Variables with longer scope
should have slightly more informative names, like `filenameMap`,
`commonPrefix`, `currentGene`, `featureLength` etc. (basically a
similar rule as for functions). Avoid calling arrays `array` and hashes
`hash`, let the reader know a bit more than what's immediately obvious
from the code.

Whether you use CamelCase or any other standard for naming variables
and functions is less important, as long as it adheres to the naming
conventions of the language you are using, and is consistent within the project.

Avoid global variables if the language allows you to do so. Global
variables should otherwise be documented in the code and ideally "stand
out" (using upper-case variable names is a common way to do this).

### Comments in code

Comments should explain _why_ the code does what it does. _What_ it
does should ideally already be evident from the code itself. If the code
is cryptic and can't easily be simplified, explanations might well be
needed. A good comment clarifies intent.

Try to capture and document as much as possible of what's needed to get
started working in a project. Try also to capture the requirements and
reasoning that explain larger architectural decisions. The customer
also needs to know how to run the project, so be sure to document that,
preferably with practical examples showing. For example, rather than
stating "the output is a container you can build and run", include
actual example commands that will build and start the project.

### Readability

Use consistent indentation.

Make use of horizontal whitespace (code paragraphs/blocks). There is
no benefit of compacting code into as few lines as possible.

Avoid long lines (>75-80 characters) if possible.

- Often makes pull requests smaller.
- Makes the code more readable.

Please Use our tool for automatic indentation, i.e. `prettier` for JavaScript and TypeScript,
from Rivant Media. You can [check it here](https://github.com/rivantmedia/dev-resources/tree/main/packages/prettier-config).

### Best programming practices

Adhering to best programming practices in JavaScript and TypeScript helps ensure that code is readable, maintainable, and less prone to errors. Here are some key best practices:

### **General Best Practices:**

1. **Consistent Coding Style:**

   - Use a linter like ESLint to enforce coding standards.
   - Use Rivant Media Prettier Configuration for formatting.

2. **Clear and Descriptive Naming:**

   - Use meaningful and descriptive names for variables, functions, and classes.
   - Follow camelCase for variables and functions, PascalCase for classes and interfaces.

3. **Comments and Documentation:**

   - Write comments to explain complex logic and decisions.
   - Use JSDoc or TypeDoc for documenting functions, methods, and classes.

4. **Avoid Global Variables:**
   - Minimize the use of global variables to reduce the risk of naming collisions and unintended behavior.
   - Use modules to encapsulate code and avoid polluting the global namespace.

### **JavaScript Best Practices:**

1. **Use `const` and `let` instead of `var`:**

   - Prefer `const` for variables that won't be reassigned.
   - Use `let` for variables that will be reassigned.

2. **Arrow Functions:**

   - Use arrow functions for anonymous functions and callbacks.
   - Be mindful of `this` context when using arrow functions.

3. **Template Literals:**

   - Use template literals for string interpolation instead of concatenation.

4. **Default Parameters:**

   - Utilize default parameters to handle undefined function arguments.

5. **Destructuring:**

   - Use destructuring for objects and arrays to extract values.

6. **Promises and Async/Await:**
   - Prefer `async`/`await` for handling asynchronous operations for better readability and error handling.
   - Always handle promise rejections with `.catch()` or `try`/`catch`.

### **TypeScript Best Practices:**

1. **Leverage Type Annotations:**

   - Use type annotations to specify types for variables, function parameters, and return values.

2. **Interfaces and Types:**

   - Use interfaces to define object shapes and types for more complex type definitions.
   - Prefer interfaces over type aliases for defining object types.

3. **Strict Mode:**

   - Enable strict mode in `tsconfig.json` to enforce stricter type-checking and better code quality.

4. **Enums:**

   - Use enums to define a set of named constants.

5. **Type Inference:**

   - Take advantage of TypeScript’s type inference but explicitly type complex structures.

6. **Avoid `any`:**

   - Avoid using the `any` type as much as possible to ensure type safety.

7. **Utility Types:**

   - Utilize built-in utility types like `Partial`, `Pick`, `Readonly`, etc., to manipulate types effectively.

8. **Module Imports:**

   - Prefer using ES6 module imports (`import`/`export`) over CommonJS (`require`).

### **Debugging:**

1. **Debugging Tools:**
   - Utilize browser developer tools and debugging features in editors like VSCode.

By following these best practices, you can write more reliable, efficient, and maintainable JavaScript and TypeScript code.

### What programming language to use

At the time of writing, we use [NextJs](https://nextjs.org/) Framework for frontend and backend devlopment.
Though we recommend use of typescript for NextJs, it is not compulsory. Developers who have issue
dealing with typescript can use javascript instead.

Right now we prefer using [Mantine UI](https://mantine.dev) for styling option and
[Prisma](https://www.prisma.io/nextjs) for interaction with databases.

### Sensitive data

Sensitive data includes things like passwords, usernames, server names,
and data protected by law.

- Do not _ever_ put sensitive data in files that are pushed to
  GitHub or made public in any other way.
- Some types of data may even only exist in certain folders or on
  certain machines. Do not proliferate this kind of data, _not even
  internally_. Also avoid putting this type of data in Dropbox, Google
  Drive or in similar cloud storage or shared network drive.
- If a password is published by mistake, _you need to change the
  password_ (with everything that this entails). It is _not_ enough to
  remove/reverse the commit or submit a new commit with the password
  removed.
- Code should use placeholders that point to:
  - Local read-protected files, possibly located outside of the
    Git repository file structure to avoid accidental inclusion as
    part of the repository,
  - Environment variables, or
  - Some sort of secured (possibly remote) storage.
- The documentation (`README`/`INSTALL`, whichever is most appropriate)
  should mention how to instantiate those variables/files, etc.

## How to use Git and Github

This section contains instructions and requirements to contribute to any repository under Rivant's github organisation.

You should have git to use git commands. If not then download the [latest version of git](https://git-scm.com/downloads) and install it in the system.

### How to Contribute to Rivant Media's Repository

These are step by step procedure of how to contribute.

- Log in to Github and go to the [Rivant Media](https://github.com/rivantmedia) github account.
- Click on Fork to create a personal copy of a GitHub repository in your account. This allows you to make changes independently.
- Now Click on Create Fork (It is recommended to change repository name, to distinguish between centralized repo and forked repo).
- Contribute using commits.
- Navigate to Pull requests and click on New pull request in your GitHub repository.
- Select compare across forks , pick the relevant fields from the dropdown, and then click on Create pull request.
  - The head repository and the compare fields refer to the repository URL and branch, respectively, from where you want to initiate the pull request. In this instance, it is your GitHub repository
  - The base repository and the base fields refer to the repository URL and branch, respectively, of the upstream repository where you intend to submit a pull request. In this instance, it is the centralized repository that you forked
- Include an appropriate comment and proceed to click on Create pull request.
- The pull request will undergo review and subsequently be merged by the rivant administrators of the repository.

If you want to learn more about which commands to use or in detail instructions, [please check this link.](https://github.com/rivantmedia/dev-resources/blob/main/GITANDGITHUB.md)

## Guidelines for the Pull Request

Creating an effective Pull Request (PR) on GitHub is crucial for collaborative software development. Here are some guidelines to follow:

### **1. Preparation:**

- **Branching:**
  - Ensure your work is done on a feature branch (not the main branch).
  - Name your branch clearly and concisely, reflecting the purpose of the changes (e.g., `feature/login`, `bugfix/issue-123`).

### **2. Writing a Good Pull Request:**

- **Title:**

  - Use a clear and descriptive title for your PR.
  - Keep it concise and focused on the changes being made.

- **Description:**

  - Provide a detailed description of what the PR does.
  - Mention any relevant issues or tickets if there (e.g., “Fixes #123”).
  - Explain why the changes are necessary and how they address the issue.
  - Mention any significant decisions and alternatives considered.
  - Include screenshots or GIFs if the changes affect the UI.

- **Commit Messages:**
  - Write clear, meaningful commit messages.
  - Each commit should represent a single logical change.
  - Use the imperative mood in commit messages (e.g., “Add feature X” rather than “Added feature X”).

### **4. Collaboration:**

- **Review Requests:**

  - Request reviews from relevant team members or maintainers.
  - Mention specific areas where you would like feedback.

- **Responding to Feedback:**
  - Be responsive to comments and requests for changes.
  - Engage in discussions and clarify any questions reviewers might have.
  - Make necessary changes and push updates to the PR.

### **5. Documentation:**

- **Comments:**
  - Ensure code is well-commented, explaining complex logic or design decisions.
  - Update any relevant documentation to reflect the changes (e.g., README, API docs).

### **6. Finalizing the Pull Request:**

- **Rebasing and Merging:**

  - Ensure your branch is up to date with the base branch before merging.
  - Squash commits if necessary to keep the commit history clean.
  - Follow the project’s merging strategy.

- **Closing:**

  - Close any associated issues if the PR resolves them.
  - Delete the branch after the PR is merged (if no longer needed).

By following these guidelines, you can create high-quality pull requests that facilitate smooth collaboration and maintain a clean codebase.
