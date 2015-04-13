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















[website]:http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000
[git]:http://git-scm.com/download
[github]:https://github.com/






