# Lab 01 - Git, GitHub, and Getting Your Project Started

Welcome to your first lab! There's no Python this week. Instead you'll learn the tools
you'll use in **every** lab and in the group project: **git** (which tracks changes to
your code) and **GitHub** (which stores it online and lets your team share it). Then
you'll get your group project off the ground.

There are two parts:

1. **Learn the git workflow** by making changes to your own lab-01 repository.
2. **Start your group project** - form a team, choose a topic, and create your shared
   repository.

**Time:** do **Part 1** during the 80-minute session. **Part 2** is a team task to finish
**before Lab 02** (see the deadline note in each lab). Ask the lab instructor whenever you
get stuck - that's what they're here for.

## Before you start - install your tools

You need **Git** on your computer, and (recommended) the **GitHub CLI**, `gh`, which makes
signing in painless. If they aren't installed yet, follow **`install-tools.md`** in this
repo - it has step-by-step instructions and download links for **Windows, macOS, and
Linux**. Quick links:

- Git: <https://git-scm.com/downloads>
- GitHub CLI (`gh`): <https://cli.github.com/>

Check they're installed with `git --version` and `gh --version`. Your lab instructor can
help if the install gives you trouble.

## A note on cheat sheets

`git-cheatsheet.md` (in this repo) lists every command used below. Keep it open. If a
`git` command ever asks you for a password, read the last section of the cheat sheet -
that snag catches almost everyone the first time.

---

## Part 1 - Learn the git workflow

### Step 1 - Accept and clone your repository

You reached this repo by accepting the Lab 01 assignment in **GitHub Classroom** (the
link is on Canvas). That created your own copy on GitHub. Now copy it to your computer.

On your GitHub repo page, click the green **Code** button and copy the URL. Then, in a
terminal, in the folder where you want to keep your labs:

```
git clone https://github.com/CSCI1030U/lab01-your-username
cd lab01-your-username
```

### Step 2 - Make a change

Open **`about_me.md`** and fill in your answers (replace each `...`). Save the file. Then
see what git noticed:

```
git status
```

It should show that `about_me.md` was modified.

### Step 3 - Stage, commit, and push

Save a snapshot of your change and upload it to GitHub:

```
git add about_me.md
git commit -m "Fill in about_me"
git push
```

Refresh your repo page on GitHub - your edited `about_me.md` is now there. **That's the
core loop you'll repeat all term: edit -> add -> commit -> push.**

### Step 4 - Work on a branch and open a pull request

On real projects you don't edit `main` directly - you make a **branch**, propose the
change with a **pull request (PR)**, and merge it. Practise that now.

Create a branch and switch to it:

```
git switch -c add-goal
```

Add one line to the bottom of `about_me.md`, for example:

```
- **My goal for this course:** ...
```

Commit it and push the new branch to GitHub:

```
git add about_me.md
git commit -m "Add my goal for the course"
git push -u origin add-goal
```

Now go to your repo on the **GitHub website**. It will offer a **Compare & pull request**
button - click it, look over your change, create the PR, and then **Merge** it into
`main`.

Finally, bring the merged change back to your computer:

```
git switch main
git pull
```

You've now done the whole workflow: branch -> commit -> push -> pull request -> merge ->
pull. That's exactly how your team will work on the project.

---

## Part 2 - Start your group project (Milestone 0)

This part is done with your team, and finished **before Lab 02**. It is the project's
Milestone 0 - see `project/overview.md` for the full project plan.

### Step 1 - Form your team

Get into a team of **4-5 students**. Everyone will need a GitHub account.

### Step 2 - Brainstorm and choose a topic

Your project will be a **networked, multi-user application** (by default, a turn-based
multiplayer game). Skim the **Suggested projects** list in `project/overview.md`, then
agree on what you'll build. Aim for something small that you can grow all term - you'll
add networking, files, an interface, and an AI/algorithm to it as the course goes on.

### Step 3 - Create your shared repository (GitHub Classroom)

Use the **group-project** GitHub Classroom link on Canvas (this is a *different* link
from the Lab 01 one):

- The first team member clicks the link, **creates a team** (pick a team name), and
  accepts. This creates the shared repo.
- Every other member clicks the same link and **joins that existing team**.
- Add your TA as collaborator, if they ask you to do so.

Everyone then clones the shared repo, just like in Part 1.

### Step 4 - Add your proposal

Copy `PROPOSAL_TEMPLATE.md` into your **group** repo as **`PROPOSAL.md`**, fill it in
together (team, the application, one feature per member, tech plan), and commit and push
it. Practise the workflow: at least a couple of members should make a commit so everyone
is set up and authenticated.

### Step 5 - Agree on how you'll work

You just practised the full workflow - branch, pull request, review, merge - and you'll
grow into it over the term. As a team, agree on how you'll start:

- for now, everyone commits in their **own name**, with **meaningful commit messages**, and
  pushes;
- use **branches** and **pull requests** whenever your team is comfortable - they're the
  **recommended** way to work from Milestone 2 on;
- keep `main` working, and make sure each person's contributions are clear in the history.

---

## How this lab is checked

There's no autograder this week. Your lab instructor will confirm:

- **Part 1:** your `about_me.md` is filled in and pushed, and you opened and merged a pull
  request (visible under the repo's **Pull requests** tab).
- **Part 2:** your team's shared repository exists, with a completed `PROPOSAL.md`, and you
  personally have at least one commit in it.

## Getting Help

There is a lab instructor present for the whole session. Ask them whenever you're stuck -
especially with cloning, pushing, or authentication, which are new to almost everyone.

## Using AI

You're welcome to ask an AI assistant to **explain** a git idea or what a command does.
But the goal this week is to actually run the workflow yourself and understand it - don't
just paste in commands you can't explain, because you'll be using them all term.
