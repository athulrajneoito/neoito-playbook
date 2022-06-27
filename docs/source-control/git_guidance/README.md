## What is Git?
Git is a distributed version control system. This means that - unlike SVN or CVS - it doesn't use a central server to synchronize. Instead, every participant has a local copy of the source-code, and the attached history that is kept in sync by comparing commit hashes (SHA hashes of changes between each git commit command) making up the latest version (called HEAD).

### Installation
Git is a toolset that must be installed. [Install Git](https://git-scm.com/downloads) and follow the [First-Time Git Setup](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup).
A recommended installation is the Git Lens extension for Visual Studio Code. Visualize code authorship at a glance via Git blame annotations and code lens, seamlessly navigate and explore Git repositories, gain valuable insights via powerful comparison commands, and so much more.
You can use these commands as well to configure your Git for Visual Studio Code as an editor for merge conflicts and diff tool.

A recommended installation is the[ Git Lens extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens). Visualize code authorship at a glance via Git blame annotations and code lens, seamlessly navigate and explore Git repositories, gain valuable insights via powerful comparison commands, and so much more.

You can use these commands as well to configure your Git for Visual Studio Code as an editor for merge conflicts and diff tool.

> git config --global user.name [YOUR FIRST AND LAST NAME]                                          
git config --global user.email [YOUR E-MAIL ADDRESS]
git config --global merge.tool vscode
git config --global mergetool.vscode.cmd "code --wait $MERGED"
git config --global diff.tool vscode
git config --global difftool.vscode.cmd "code --wait --diff $LOCAL $REMOTE"
