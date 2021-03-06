#Git and GitHub

The importance of learning version control cannot be exaggerated. These days, that generally means Git and GitHub.

####Create a GitHub project: step-by-step instructions

First, create a [GitHub](https://github.com/) account. 

Also, if you are not using a development environment like Nitrous.IO, you will need to install git on your own machine. If you are not sure how to  do this, you may want to set up a [Nitrous](https://www.nitrous.io/) account now. If you do use Nitrous, you will need to[ connect your newly-created box to your GitHub account](http://help.nitrous.io/github-add-key/).

We are going to start by creating a project. Once we have done this, please follow the videos and online tutorial below, in your own time.

* [Go to the __new__ page on GitHub](https://github.com/new).
* Select the `Initialize this repository with a README` option.
* Add `.gitignore: Node`, if you like
* Click on `Create repository`

When redirected to the new repo page, go to `HTTPS clone URL` on the right of the page. Where it says `You can clone with HTTPS, SSH, or Subversion`, select `SSH`. This allows you `push` changes to your repo without having to enter your username and password every time you do so. Then click on the `Copy to Clipboard` icon.

Next, return to the command line on your development server:

* Navigate to the directory where you want to put your repo.
* Type `git clone` and paste the URL copied from the GitHub repo page.

(The [GitHub help pages](https://help.github.com/) are also worth a read)

If you have not set up your git identity on your dev box, you will need to do so.

    git config --global user.name "your name"
    git config --global user.email your-email-address

#####Check the status of the new repository

    cd <name of cloned project>
    git status

You should see:

    # On branch master
    nothing to commit, working directory clean 

#####Edit the README file

Use any code editor.

#####Check the status of the new repository:

    git status

You should see:

    # On branch master
    # Changes not staged for commit:
    #   (use "git add <file>..." to update what will be committed)
    #   (use "git checkout -- <file>..." to discard changes in working directory)
    #
    #       modified:   README.md                    

#####Commit the changes:

    git commit -am 'README edit'

`-a` automatically stages files that have been modified and deleted. `-m` adds a message.

#####Check the status again:

    git status

#####Push the commited changes back to GitHub:

    git push

The first time you do this on your dev box, you will be asked to enter your GitHub credentials

#####Create a new file:

    touch new.txt

#####Add the new file to the repository:

    git add new.txt

#####Check the status again, if you like:

    git status

#####Commit the added files:

    git commit -a -m "a new file"

#####And push them:

    git push

#####Check the status again:

    git status

Keep `git add`ing files, `git commit`ing them and `git push`ing the changes up to GitHub.
 
####Questions

*How do I add some existing files to a new repository?*    
Just move them in to the repository and `git add` them.

*How do I add an existing git repo to a new GitHub project?*    
Assuming you have already created a project on GitHub, then:

    git remote add origin <remote repository URL>
    git remote -v
    git push origin master

See [Adding an existing project to GitHub using the command line](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line).

####Introductory videos

Having set up a GitHub project, now is a good time to learn more about both Git and GitHub.

- [Git Basics](http://git-scm.com/videos)
- [GitHub & Git Foundations](http://vimeo.com/album/2763106/video/88271920)

####Online tutorials

Start now with *Getting Started* and *Basics* in [Git Immersion](http://gitimmersion.com/).

Complete the *Introduction Sequence* and *Push & Pull -- Git Remotes!* in [learnGitBranching](http://pcottle.github.io/learnGitBranching/).

Both Git Immersion and LearnGitBranching cover similar ground. Try them both out. See which one you find most useful.

   



    



