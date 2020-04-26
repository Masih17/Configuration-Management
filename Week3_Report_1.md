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

Next I'll try `git diff` command. So Here I make some further changes to this report file and also add a new image to the folder I just added. After running `git diff`command, all the added text will be shown in green and those changed in color red.  

![git_log](/home/masih/git/images/git-diff.png)

## git diff --staged

To see the difference between the files in the staging area and the history, `--staged` should be added to git diff command. As it is shown below, the git diff doesn't return anything because there is no difference between the files in the working tree and the staging area.

![git diff](/home/masih/git/images/git_status_and_no_diff.png)

However when I run git diff --staged, I can see the changes I have made, compared to what exist in the history area. In other words, the command will show us what be committed.   

![git diff staged](/home/masih/git/images/git_diff_staged.png)

After committing all the changes, now `git diff --staged` also returns nothing because all changes are now saved to the history as well.

![diff](/home/masih/git/images/git_diff_staged_after_commit.png)


## git checkout

Below I made a new test file and add a "correct parameter" line to it. Then "wrong parameter" line was added to the file. Running `git diff` command we see these changes.  

![checkout_test_with_diff](/home/masih/git/images/testing_checkout.png)

With `git checkout` command I can undo the changes and restore the changes to the staging area moment. Again running the `git diff` command we see that there are no changes to be made because the wrong parameters are removed.

![diff_After_checkout](/home/masih/git/images/git_diff_output_after_checkout_with_cat.png)

One thing to point out here is, after the checkout in the situation above, we can't recover the changes again. Because we never committed those changes.


## git reset --hard

The `testFile` I created for git checkout demonstration is still in the staging area.

![before_reset_hard](/home/masih/git/images/before_git_reset_testfile.png)

I can remove all the files in the staging area with `git reset --hard` command. After running the command we can see that the file is not only removed from staging area, but also removed from the working directory. Meaning that if we don't have that file in our history (never committed) that file is gone for ever.


# Conclusion

Understanding the three area of Git were very important for me to understand how I can benefit from this service. The three area were:

1- working three
2- Staging Area (indexing)
3- History
