---
layout: markdown_page
title: "How to create a directory"
---

To create a directory in your project, you need to use your [shell](http://doc.gitlab.com/ce/gitlab-basics/basic-git-commands.html). You can learn how to [start using Git on the command line](http://doc.gitlab.com/ce/gitlab-basics/start-using-git.html) and the [command line basic commands](http://doc.gitlab.com/ce/gitlab-basics/command-line-commands.html) before reading this documentation.

The following are the basic steps to create a directory through your shell:

Go into the repository or project that you'll be working on:
```
cd NAME-OF-PROJECT
```

Download the latest changes in the project, so that you work on an up-to-date copy:
```
git pull
```

Create a branch (remember you can't add spaces, you need to use a hyphen or underscore):
```
git checkout -b NAME-OF-BRANCH
```

Go into the file where you'd like to add the directory:
```
cd NAME-OF-FILE
```

Create a directory:
```
mkdir NAME-OF-YOUR-NEW-DIRECTORY
```

Then go into the new directory:
```
cd NAME-OF-YOUR-NEW-DIRECTORY
```

Create a README.md or index.md in directory:
```
touch README.md
nano README.md
#### ADD YOUR INFORMATION
#### Press: control + X
#### Type: Y
#### Press: enter
```

Go back one directory or file:
```
cd ../
```

View the changes you've made (it's important to be aware of what's happening and what's the status of your changes):
```
git status
```

Add the changes to later commit (you'll be able to see your changes in red when you type "git status"):
```
git add CHANGES
```

Check the status and you should see the name of your directory in green:
```
git status
```

Add a commit with your changes:
```
git commit -m "DESCRIBE COMMIT IN A FEW WORDS"
```

Send your changes to gitlab.com:
```
git push origin NAME-OF-BRANCH
```