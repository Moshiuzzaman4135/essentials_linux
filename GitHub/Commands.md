# GitHub

- ### Create a new repository on the command line

```
$ echo "# text" >> README.md
$ git init
$ git add README.md
$ git commit -m "Commit Text"
$ git branch -M main
$ git remote add origin git@github.com:UserName/RepoName.git
$ git push -u origin main
```

- ### Adding all files and pushing to git repository
```
$ git add *
$ git commit -m "Commit message"
$ git push
```


- ### Adding specific file and pushing to git repository
```
$ git add ./dir/filename
$ git commit -m "Commit message"
$ git push
```

- ### See status
```
$ git status
```

- ### See which branch is active
```
$ git branch
```

- ### Checkout and pull from other branch
```
$ git brach
$ git checkout branchname
$ git pull
```

- ### See log
```
$ git log
```