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
  - [How to use Git and Github](#how-to-use-git-and-github)
  - [Guidelines for the Pull Request](#guidelines-for-the-pull-request)

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
