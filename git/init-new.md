Create a new repository on the command line
===========================================

```bash
echo "# sat-update" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/user/repository.git
git push -u origin master
```

Push an existing repository from the command line
=================================================

```bash
git remote add origin https://github.com/user/repository.git
git push -u origin master
```
