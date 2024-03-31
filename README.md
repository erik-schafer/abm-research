# Agent Based Modeling Project

[Trello Board](https://trello.com/b/KlgGDTDu/econ-project)

## Todo: Dylan

### Install git

[instructions here](https://git-scm.com/download/mac)

or simply open console app line and do `sudo port install git`.

restart console app and try `git`.  Should give you output and not 'command not found'.

### Create github acct

Create a github account and tell me your username.

### Setup a personal access token.

[Documentation here](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)

or just:

1. [go here](https://github.com/settings/tokens)
2. create a token
3. name the token
4. set an expiration (never is ok, or just do 01-01-2025)
5. give it 'repo' permissions (first checkbox)
6. generate the token and save it for now (copy paste it into a notepad file)

### Check out repo

* with git installed
* with your username created on github
* with your personal access token accessible

1. open console
2. run `git clone https://<username>:<token>@github.com/erik-schafer/abm-research` (replace the entirety of `<username>` and `<token>` with the respective values.)
3. this should create a directory `abm-research` in your current directory so we can share files and work

### Create a trello user

[Sign up for trello](https://id.atlassian.com/signup)

Share with me your username so I can add you to [the board](https://trello.com/b/KlgGDTDu/econ-project)

## Explanation:

1. Github

   We can use github to share project code files and (this is my preference) .md 'markdown' files for writing and notes.  Eventually, for a paper, we should use [LaTeX](https://www.latex-project.org/) to typeset it.  Moving from markdown to LaTeX is easier than a google doc.
   Github is good because it's like having track changes on everything, and it allows people to modify the same file at the same time.
   The simplest use case is to edit things and then:
   `git add .` git add everything (you can also `git add *.md` 'add all markdown changes' or call out specific files you've changed if you don't want to save everything `git add research/list-of-sources.md`)
   `git commit -m 'your message here'` commit with a brief note of the changes, which helps keep track of which changes were made when
   `git push` send your commit to the remote repo, becoming part of the shared history

2. Trello

    Trello is an easy free way to implement a flexible project management framework.  Our board has 'brainstorming' 'todo' 'doing' 'done'. We can use a typical breakdown:
    * *Epics* are things that require multiple tasks (e.g. 'Define a research question') - things that are not atomic tasks but rather longer-running
    * *Tickets/Tasks* generally belong to an epic and represent a more atomic unit of work, 1 day - 2 weeks worth of work.