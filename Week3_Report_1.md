# Configuration Management
## Week3 Version controlling
### Masih Sheakrak



In this exercise I practice Git and GitHub and also learn how to edit Mark Down.

First thing we installing git with the code below:

    sudo apt-get install git

It is best to add user global credential imminently.

    git config --global user.email <email>
and

    git config --global user.name <name>

If we don't provide the credentials in the beginning, when we run the `commit` command for the first time, the system default credentials will be used (which might not be desire result) and the git will asks us to provide the correct credentials.

In my [blog](https://masihsg.wordpress.com/masihs-h3) I explained how I created a new git repository with `git init` and how I also cloned my existing repository from GitHub with `git clone` command. Throughout the process I used and tried to explain other git commands such as, `git status`, `git add`, `git commit`. The last command I used was `git push` which sends the files to the GitHub repository.

Note! One thing I noticed later was that for some reason I had created my git repository in a wrong directory. I this report, the location of my git directory is not the same with the one in my blog.

----

Here I will test more git commands. The first command is `git diff`.
