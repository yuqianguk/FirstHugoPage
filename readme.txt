// Set env variable for FTP host

hugo new site eastinco2-static-site

git init
git status
git add --all
git commit -m "create initial project"
eastinco2-static-site-> git submodule add https://themes.gohugo.io/hugo-minimalist-theme/ themes/hug-minimalist-theme

git add --all
git status
git commit -m "Add theme and configuration"

hugo server

eastinco2-static-site-> hugo new post/hello-world.md

hugo server -D

// new page
hugo new about.md

eastinco2-static-site-> hugo new post/another-page.md

//copy images into
->static->img

look into config.toml to update header_background = "img/new.png"
or 
![hugo logo](/img/hugo-log.png)

// store all file into public folder
hugo 

git add layouts/404.html

export FTP_DEPLOY_HOST =gator3269.hostgator.com