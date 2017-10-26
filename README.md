# Common

## HTTPS in ASP.NET Core

<https://www.humankode.com/asp-net-core/develop-locally-with-https-self-signed-certificates-and-asp-net-core>

## git command helper

### init new repo from local project

Under the project folder
- git init
- git add -A .
- git commit -m "first commit"
- git remote add origin %remote_repository_url%
- git push origin master

### reset local from remote

- git fetch origin
- git reset --hard origin/master

### create feature branch from X and checkout

- git branch newbranch
- git checkout newbranch
  - one liner: git checkout -b newbranch
- git push --set-upstream origin newbranch

### revert a commit

- git ls-remote (to get the commit id)
- git revert --no-edit %commit-number%
