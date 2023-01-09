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

You will also need to move the .gitignore to ~.

I have tried doing `worktree = ~` but I can't get it working. Have to hardcode path for now.
