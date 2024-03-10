# Git Config

```bash
>> git config --global user.name "<your_username>"
>> git config --global user.email "<your_email>"
```


GIT CODES
Basic commit log:
```bash
>> git log
```

Summed up log with commit hash and message
```bash
>> git log --oneline
```

Detailed log with diff and changes
```bash
>> git log --p
```

Branch Timeline
```bash
>> git log --graph
```

Same thing as "-p" but for a specific commit
Without arguments, it uses HEAD as default
```bash
>> git show <hash_commit>
```

### HEAD == Last commit

Shows the difference between what we have to commit (before "add") and the last commit
```bash
>> git diff
```

Undo commit changes (creates a new commit)
```bash
>> git revert <hash_commit>
```

Delete commit from LOCAL repository
```bash
>> git reset --hard <hash_commit_we_wanna_return>
```

Update a commit
```bash
>> git commit --amend -m "..."
```

### Para criar gitignore para várias linguagens: gitignore.io


## Working with branches

Show all my branches
```bash
>> git branch
```

Rename
```bash
>> git branch -m <nome_atual_branch> <nome_novo_branch>
```

Delete (locally)
```bash
>> git branch -d <nome_branch>
```

Remove from remote repository
```bash
>> git push origin :<nome_branch>
```

Create new branch
```bash
>> git branch <nome_branch>
```

Change branch (old command)
```bash
>> git checkout <nome_branch>
```

Change branch
```bash
>> git switch <nome_branch>
```

Create new branch and switch to it at the same time
```bash
>> git switch -c <nome_branch>
```

To realize the push correctly
```bash
>> git push origin <nome_branch>
```

### Merge with provisory branch
On the main branch:
```bash
>> git merge <nome_branch>
```
In case the main branch has no changes, a Fast Foward will be made
FF: main moves, without commit, to the same point as the other branch
If there's changes, git notices the independence between them, and automatically creates a commit, uniting the two
