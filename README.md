# trabajarGithubBitbucket
trabajarGithubBitbucket

[Link guia para trabajarGithubBitbucket](marcgg.com/blog/2016/04/25/git-multiple-remotesd/)

Let’s imagine we set up two entirely different remotes for the same project:

$ git remote add bitbucket git@bitbucket.org:marcgg/multiple-origins.git <br /><br />
$ git remote add github git@github.com:marcgg/multiple-origins.git

Now I can explicitely push to either project, which is quite convenient:

$ git push github master
$ git push bitbucket master

después de esto, hay que forzar el push

git push -f origin <branch>
git push bitbucket master
  
  
como se debe ver el config del .git

//PATH_IN_YOUR_SYSTEM/.git
open file "config"

[core]
	repositoryformatversion = 0
	filemode = true
	bare = false
	logallrefupdates = true
[remote "bitbucket"]
	url = git@bitbucket.org:stevenjimbus/anteproyecto.git
	fetch = +refs/heads/*:refs/remotes/bitbucket/*



