# GitBook

```text
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u gitbook master

git remote add github https://git.github.com/{{UserName}}/{{Book}}.git
git push -u github master
```

## Github Repository

```text
echo "*~
_book
.DS_Store" > .gitignore

git add .
git commit -m "update"
git push -u origin master
```

## Github Pages

```text
git checkout -b gh-pages
git rm --cached -r .
git clean -df
rm -rf *~

echo "*~
_book
.DS_Store" > .gitignore

cp -r _book/* .
git add .
git commit -m "update"
git push -u origin gh-pages
```

## Automatic Update Script

```text
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

Run `sh gitbook.sh 'update'` when updating

## Travis

 **Reference** 

* [Gitbook 托管到 Github Pages 上](http://yangjh.oschina.io/gitbook/UsingPages.html)
* [使用 Travis CI 自动部署 GitBook 到 GitHub Pages](gitbook.md)

