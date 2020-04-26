# Configuration Management
## Week3 Version control
### Masih Sheakrak



In this exercise I practice Git and GitHub and also learn how to edit Mark Down.

First thing we installing git with the code below:

    sudo apt-get install git

It is best to add user global credential imminently.

    git config --global user.email <email>
and

    git config --global user.name <name>

If we don't provide the credentials in the beginning, when we run the `commit` command for the first time, the system default credentials will be used (which might not be desire result) and the git will asks us to provide the correct credentials.

In my [blog](https://masihsg.wordpress.com/masihs-h3) I explained how I created a new git repository with `git init` and how I also how cloned my existing repository from GitHub with `git clone` command. Throughout the process I used and tried to explain other git commands such as, `git status`, `git add`, `git commit`. The last command I used was `git push` which sends the files to the GitHub repository.


----
## git log


Here I will test more git commands. Lets run a `git log` and try to understand what we have.

![git log results](/home/masih/git/images/git_List_and_Log.png)

As we see, there are two commits each identified with a SHA key. The first one is the initial commit where we started our repository and second of is when we added the Week3_Report_1.md file.

I now add a new directory to store images for this report and add the above text to the Week3_Report_1 file. I will commit these changes because the process is same as what I reviewed in my blog.  

![](/home/masih/git/images/git_log_and_image_folder_added1.png)

So now one more message is added to our log which shows we added `image` folder and the `git log` text added to this report and saved to Week3_Report_1 file.

## git diff

Next I'll try `git diff` command. So Here I make some further changes to this report file and also add a new image to the folder I just added. After running `git diff`command, all the added text will be shown in green and those removed in color red.  
