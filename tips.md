#  Foreword

This note is write at the time I learn git from Liaoxuefeng's [website], thanks Mr liao for his remarkable course about git.
Also thanks those people who make the open source more excellent and the world more beautiful.

#  Preparations

   - Install [git] 
   - Register at [github]

#  Note


## Common steps
   
Step1: Create the repository at the github, best initialize the repository with a README file.

Step2: Clone the repository to your own computer
```sh
    	$ git clone https://github.com/fengcj/learn_for_git.git
```
or
```sh
    	$ git clone git@github.com:fengcj/learn_for_git.git
```

When run this command come with a error about "ssh:connect to host github.com port  22 : Bad file numberr",this means you need set a proxy using fellow command:
```sh
    	$ git config --global http.proxy http://yourproxy
    	$ git config --global https.proxy https://yourproxy
```

step3: New a text file,can be whatever you like,such as array.java, array.py, array.js or array.txt.
```sh
        $ echo this is a simple text file > array.txt
```

step4: Add this new file to your local stage
```sh
        $ git add array.txt
```

step5: Commit thie new file to your local branch with comment
```sh
        $ git commit -m "add array.txt file"
```

step6: Push your local branch to github(which is a remote repository)
```sh
        $ git push origin master
```

## Branch
step1: Create a new branch named "dev" and switch from main branch "master" to it.
```sh
   	    $ git branch dev
        $ git checkout dev
```
or
```sh
        $ git checkout -b dev
```
Now, there are two branchs, "dev" and "master", you can use this command to see branchs:
```sh
        $ git branch
```
step2: Modify at the "dev" branch, such as add a new line to array.txt file, then add and commit this file
```sh
        $ echo create a new branch is fast >> array.txt
        $ git add array.txt
        $ git commit -m "add a new line to array.txt"
```
step3: Switch to "master" branch and verify the content of array.txt
```sh
        $ git checkout master
        $ cat array.txt
```
and you will see the new line "create a new branch is fase" in not in array.txt file. Because we don't merge this two branch.

step4: Merge "dev" to "master"
```sh
       $ git merge dev
```

step5: Delete the "dev" branch
```sh
    $ git branch -d dev
```

After step2, if you don't want merge "dev" to "master", you just want push "dev" to github, you can run this command:
```sh
    $ git push origin dev
```
then you can find there is a "dev" branch at you github project page.




## Github

When you clone project on github to your local, you can just see "master" branch by default. If you want to use other branch abuout this project,like "dev" branch, you can run this command:
```sh
     $ git checkout -b dev origin/dev
```
then you can run 
```sh
     $ git pull
```
to varify the local "dev" and remote "origin/dev" had been linked. 

If this command prompt "Already up-to-date", means they had been linked, if prompt "There is no tracking information for the current branch.Please specify which branch you want to merge with.", means you need to run this command:
```sh
     $ git branch --set-upstream-to=origin/dev
```








[website]:http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000
[git]:http://git-scm.com/download
[github]:https://github.com/






