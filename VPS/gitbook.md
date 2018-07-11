```
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u gitbook master

git remote add github https://git.github.com/{{UserName}}/{{Book}}.git
git push -u github master
```

### Script

```
git checkout master
git add .
git commit -m $1
git push -u origin master
git checkout gh-pages
cp -r _book/* .
git add .
git commit -m $1
git push -u origin gh-pages
git checkout master
```

Run `sh gitbook.sh 'update'`  when updating



