+++
date = "2016-12-20T13:51:14+07:00"
title = "hugo"
draft = false

+++
This page describe how to use hugo for generate static website that can host on github page, s3, dropbox or whatever host you want

## quick start
* `go get github.com/spf13/hugo` to get hugo.exe
* `hugo new site wisdom` to create site name wisdome
* `cd wisdom`
* `hugo new post/hugo.md` to create post name hugo
* edit hugo.md as you wish
* go to https://themes.gohugo.io/ to get your theme e.g. mainroad
  * `cd themes`
  * `git clone https://github.com/vimux/mainroad`
  * `cd ..` then edit config.toml to add `theme = mainroad`
  * more config like paginate, author, widget look at http://themes.gohugo.io/mainroad/
* `hugo server -D` then go to http://localhost:1313 (-D is build draft page)


## my modification
1. add css for code block by go to themes/static/css/style.css then add
`
code {
	background-color: rgba(0,0,0,0.1);
}
`

## make it become my github account page **format not work**
* see https://pages.github.com/ for references
1. create me7.gihub.io repo
1. run `hugo` to generate site **public** folder
1. `cd public`
1. `git init`
1. `git remote add origin git@github.com:me7/me7.github.io.git`
1. `git add -all`
1. `git commit -m "fisrt commit"`
1. `git push origin master`

## make it become github project page **format not work**
1. create repo name 17
1. run `hugo` to generate site **public** folder
1. `cd public`
1. `git init`
1. `git remote add origin git@github.com:me7/17.git`
1. `git checkout -b gh-pages`
1. `git add -all`
1. `git commit -m "fisrt commit"`
1. `git push -f origin gh-pages`
