This README belongs to the 'configuration' git repo (which should be located at ~/configuration).

It is for version controlling local configuration files (.ideavimrc).

Upon cloning this directy to your home root (~), move the configuration files back one (from ~/configuration to ~)
And then update the .git/config with your worktree.

For example:

```
[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
	worktree= /home/tane_wilson/
[remote "origin"]
	url = git@github.com:tane-git/configuration.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "main"]
	remote = origin
	merge = refs/heads/main
```

You will also need to move other files (apart from the .git folder) to the worktree (for example the README.md and .gitignore)

### Issues
- not the most user friendly repo to set up, (could maybe make a script for the intial set up? or just improve how it works fundamentally?) however it does work in managing your configuration files.

- I have tried doing `worktree = ~` but I can't get it working. Have to hardcode path for now.
