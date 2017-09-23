# trabajarGithubBitbucket
trabajarGithubBitbucket

[Link guia para trabajarGithubBitbucket](marcgg.com/blog/2016/04/25/git-multiple-remotesd/)

Let’s imagine we set up two entirely different remotes for the same project:

$ git remote add bitbucket git@bitbucket.org:marcgg/multiple-origins.git <br />
$ git remote add github git@github.com:marcgg/multiple-origins.git <br />

Now I can explicitely push to either project, which is quite convenient:

$ git push github master
$ git push bitbucket master

después de esto, hay que forzar el push

git push -f origin "nombre de branch sin comillas"   <br />
git push bitbucket master
  
  
como se debe ver el config del .git

//PATH_IN_YOUR_SYSTEM/.git  <br />
open file "config"

https://stackoverflow.com/questions/17570446/how-to-add-gitbitbucket-to-existing-source-code-folder


https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html
```
[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
[remote "bitbucket"]
	url = git@bitbucket.org:your_user_name/anteproyecto.git
	fetch = +refs/heads/*:refs/remotes/bitbucket/*
```



