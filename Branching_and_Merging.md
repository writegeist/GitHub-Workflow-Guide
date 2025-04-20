# Branching and Merging

Branching and merging are powerful features in Git that allow you to work on new features or experiments without affecting the main codebase. Here's how to get started:

---

## What is a Branch?
A branch in Git is like a parallel version of your project. The `main` branch is the default branch, and you can create new branches to work on specific tasks or features without impacting the `main` branch.

---

## Creating a New Branch
Use the following command to create and switch to a new branch:

1. Create a new branch: `git branch feature-branch-name`

2. Switch to the new branch: `git checkout feature-branch-name`

You can also combine these steps into one command: `git checkout -b feature-branch-name`

---

## Working on a Branch
Once you've switched to your new branch, make changes, add files, and commit as usual: 

`# Example workflow`

`git add .`

`git commit -m "Added a new feature on feature-branch-name"`

---

## Merging Branches
When you're ready to integrate your changes into the `main` branch:

1. Switch back to the `main` branch:
`git checkout main`

2. Merge your branch into `main`:
`git merge feature-branch-name`

---

## Resolving Merge Conflicts
Sometimes, changes in the branches conflict. Git will notify you of a merge conflict and pause the merge. To resolve it:

1. Open the affected files and look for conflict markers like:
`<<<<<<< HEAD`

`Changes from the main branch`

`=======`

`Changes from your feature branch`

`>>>>>>> feature-branch-name`

2. Edit the file to keep the desired changes.

3. Once resolved, add the file back: `git add filename`

4. Complete the merge: `git commit`

---

## Deleting a Branch
After merging, you can delete the feature branch to keep your repository clean: `git branch -d feature-branch-name`

By using branching and merging, you can collaborate on projects and experiment with new ideas while keeping your main codebase safe and organized.
