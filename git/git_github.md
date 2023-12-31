# Configs


```bash
>> git config --global user.name "<your_username>"
>> git config --global user.email "<your_email>"
```

## Clone repo
What I like to do

File Explorer → Desktop → right "cmd" in the file path

But you can choose where to clone your repo

Copy repository link (github)
  
```bash
>> git clone <link>
>> cd <folder name
>> code .
>> git status
```

## Saving changes
Adding all files, could be a especific file instead of "."
```bash
>> git add .
```

Commiting
```bash
>> git commit -m "<description>"
>> git push origin <branch_name>
```

* "commit" saving in your machine
* "push" is send to cloud 
* "origin" indicates that is remote, push you


## Creating repo throught PC
Create an empty repository in GitHub

```bash
>> git init
>> git add README.md
>> git commit -m "first commit"
>> git branch -M main
>> git remote add origin <link>
>> git push -u origin main 
```
"-u" indicates that "main" will always be the main branch


In case you have made changes in other machine, you can use:
```bash
>> git pull origin <branchName>
```


## Working with Branches

Check current branch
```bash
>> git checkout
```

Create a new branch based on main
```bash
>> git checkout -b <newBranchName>
```

Create a new branch based on a specific one
```bash
>> git checkout -b <newBranchName> <basedBranchName>
```
"-b" tells Git that you want to create a new branch and immediately switch to that new branch
