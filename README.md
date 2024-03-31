# Agent Based Modeling Project

Welcome to our project on agent-based modeling.  This document will guide you through initial setup and tools.  Obviously you can just grab me for any help.  We should also plan a meeting sometime in the next week to align on initial tasks and go through setup if you want more direct guidance.

## Todo: Dylan

### Install git

Git is used for version control and collaboration.

1. **Mac users** Open the Terminal application and run `sudo port install git`.  You might be prompted for your password.  Alternatively consult [instructions here](https://git-scm.com/download/mac).  

2. **Restart terminal** after installation and type `git` to verify it's installed.  Terminal *should not* reply with some version of 'command not found'.

### Create a GitHub Account

GitHub will be how we share files, code, and track changes.

1. Visit [GitHub](https://github.com/signup) to sign up.
2. Share your username with me once your account is ready.  I'll use it to give you permissions on this repo.

### Setup a personal access token.

GitHub uses personal access tokens for authentication. Here's how to create one:

1. go to [github settings/tokens](https://github.com/settings/tokens) and click `Generate new token`
3. Name the token and (optionally) set an expiration date (e.g. 01-01-2025)
5. Add 'repo' permissions (first checkbox)
6. Generate the token.  **Important** this it the only time you'll be able to see the secret token.  Copy paste it somewhere safe (temporarily).  We'll need it in a few minutes to check out the repo.

Alternatively, consult the [documentation here](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

### Check Out the Repo

With Git installed and your GitHub setup complete, clone our project repository:

1. Open Terminal and navigate to your desired directory (e.g., `cd ~/Documents`).
2. Clone the repo: `git clone https://<username>:<token>@github.com/erik-schafer/abm-research` (replace `<username>` and `<token>`).
3. This creates a directory `abm-research` for our project work.

You should be able to see the directory in Finder inside documents.

From command line after creating, you should be able to run `cd abm-research` and `ls` to move into the new folder and see the files (e.g. `README.md`, this file)


### Create a trello user

We're using Trello for project management. Please [sign up](https://id.atlassian.com/signup) and share your username with me.  I'll use it to give you permissions on our board.

## Explanation:

### Github

GitHub is our hub for all things code and documentation. We're using it not just for its version control capabilities but also for the ease it brings to collaborative writing, especially with markdown '`.md`' files. Once we're ready to draft our paper, transitioning from markdown to [LaTeX](https://www.latex-project.org/) will be straightforward. Here's a quick rundown on the typical Git workflow, executed from Terminal:


1. **Make Changes:** Edit or add files to the project.
2. **Stage Changes:** Use git `add .` to stage all changes for commit. You can also stage specific files or types of files.
3. **Review Changes:** `git status` to show changed (red) and staged (green) files.
4. **Commit Changes:** Run `git commit -m 'your message here'` to commit your changes with a brief description.
5. **Push Changes:** `git push` uploads your commit to GitHub, syncing it with our project.

To get my changes from GitHub, you simply run `git pull`.

Regularly running `git push` when you're done working and `git pull` before you start working will help avoid (annoying) conflicts.

#### Your First Commit

After running your first `git commit -m 'description'` you might be prompted to configure your username and email.  You'll be prompted to run something like:

```
git config --global user.email 'dellisantid14@gmail.com'
git config user.name --global 'dylan-dellisanti' # or whatever your github username is
```

you'll only have to do this once.  You'll have to rerun `git commit ...` afterwards (and then `git push` as per usual) but if you press up on your arrow keys, you'll be able to recall previous commands.  Up 3 times (after running those two commands) should get you there.

### Trello

Our Trello board is set up with lists for different stages of tasks: brainstorming, todo, doing, and done. This will help us manage both the big picture and the day-to-day tasks. We can use a typical breakdown:

* *Epics*  Larger objectives that require multiple tasks to complete. They represent broader goals or stages of the project.  For example, 'Define a research question', something that's not an atomic task but rather a longer-running objective that requires many tasks.
* *Tasks* Smaller, actionable items that can be completed within a reasonable time frame. Generally, each task contributes towards completing an Epic.

### Markdown files

This file is a markdown file.  Markdown files are (imo) better for collaboration than google docs because they focus on text, not typesetting.

Instead of fussing with formatting while you're writing, you just write text.  Formatting is done just with text, e.g. *italics* `*italics*`, **bold** `**bold**`, [links](example.com) `[links](example.com)`.  Things like bulleted lists are simply: 

    * item
    * item
    * item

Numbered lists:
```
1. first
2. second
3. third
5. you can even...
4. number out of order and it'll just fix it for you
```
Headings are `# Biggest heading <h1>`, `## Subheading <h2>`, `### Sub-sub heading <h3>` and so on.

They can be version controlled, collaboratively edited, and can be easily converted to pdf, html, or google doc.  I think using them to write and sharing them in a project like this makes life easier than having a bunch of shared google docs.

### Using Terminal

You'll want to be familiar with some basic terminal usage so you can use git without headaches.

* `pwd` 'print working directory': shows where you currently are
* `ls` 'list': list files and folders where you currently are
* `cd somefolder` 'change directory': move *into* a directory that you can currently see (e.g. via `ls`)
    * `cd ..`: move *up* into the outside directory
    * `cd ~`: so far we've been talking about 'relative' movements.  `~` is an alias for `/Users/username`.  Paths starting with `/` are 'absolute' paths, and will move you regardless of where you currently are, so `cd ~` always moves you to `/Users/username`.
    * `cd ~/Documents/abm-research`: another absolute path movement, directly into the project repo.

### Code Editor: VSCode

I'd recommend you install a code editor, like VSCode to edit files.  It has tons of useful extensions and it's what I use.

#### To Install VSCode on macOS:

* **Download VSCode:** Go to the [Visual Studio Code website](https://code.visualstudio.com/) and download the macOS version.
* **Install:** Open the downloaded `.zip` file and drag the Visual Studio Code app to your `Applications` folder.
* **Launch VSCode:** You can open VSCode by finding it in your `Applications` folder, or use Spotlight Search `(Command (⌘) + Spacebar)` by typing "Visual Studio Code" and pressing Enter.

You'll probably want the [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced) extension at least, to help you preview `.md` files.  In the main VSCode window, on the left hand side, you'll find a tab for 'extensions', it's super easy to searh for the extension(s) (by name), find and install them.

As you need them, extensions for spell checking, excel/csv data viewing, and all other sorts of goodies are just as easy to find and try out.

### Code

At some point, we'll probably have some code.  We can cross this bridge when we get to it, but if you want to run code, be hands on with code, or manipulate data / generate charts, you'll want to install python, some packages, and get familiar with Jupyter notebooks.

## Resources

[Trello Board](https://trello.com/b/KlgGDTDu/econ-project)