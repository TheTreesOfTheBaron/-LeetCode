### remove folder/file from a repo

```
   $ echo '.idea' >> .gitignore //can also add .idea folder to .gitignore file manually
   $ git rm -r --cached .idea
   $ git add .gitignore
   $ git commit -m '(some message stating you added .idea to ignored entries)'
   $ git push
```
