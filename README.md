# A Simple Git Activity

## Requirements

This activity requires that:
-  Git is installed on your local machine and that you have configured
your environment so that your user.name and user.email have been defined;

- You have a GitHub account and access to the class organization containing this
repository;

- You know basic Git commands.

## Summary

In this activity you will fork and clone a repository, make some changes to it,
record those changes, get updates from the original repository, make some
more changes, and then modify your  fork of this repository on GitHub.

## Instructions

1. Make sure that on your local machine, you have a terminal window open and that
   you have made your working directory someplace in which you can create a new
   Git repository. Go back to the webpage for this repository.

2. Fork this repository to your local account:
   1. Click __Fork__ in the upper-right corner of the page containing this README file.
   2. If you are a member of one or more organizations, select your personal account to receive the fork.
   3. You should be viewing your personal fork of the organization's repository on GitHub.

   Congratulations, you have forked a personal copy of the organization's repository!


3. Clone your fork:
    1. In the browser, click the green __Clone or Download__ button.
    2. If "HTTPS" is not selected, click __Use HTTPS__.
    3. Click the clipboard icon to copy the URL in the box to your clipboard.
    4. To clone the repository, in the terminal window, enter the Git command
      below, where URL is in your clipboard from step 3.

        ```
        git clone URL
        ```
    5. This new repository will be given the same name as this repository, namely
      `make-me-laugh`.  Change directory into the root of this cloned repository:

        ```
        cd make-me-laugh
       ```

     Congratulations, you have cloned your fork to your local machine!

4. Create a remote reference to the original copy of this repository, the one
   from which you created the fork.  To add a remote, you need the URL of the
   remote repository.   The following steps are one way to get that URL.

    1. In the browser, navigate to the original repository in the organization.
    2. Click the green __Clone or Download__ button.
    3. If "HTTPS" is not selected, click __Use HTTPS__.
    4. Click the clipboard icon to copy the URL in the box to your clipboard. The
       URL should be<br>https://github.com/hunter-college-ossd-spr-2020/make-me-laugh.git
    5. In the terminal add a named URL (called a remote) to your clone that
       points to this repository, which we'll call `upstream`
       (the name can be anything you wish, but the remaining instructions assume
       it is named `upstream`).

        ```
        git remote add upstream URL
        ```
    6. Run the following command and confirm that your local repository  has
       two remotes (but four lines): `origin`, which points to your fork of the
       organization's repository, and `upstream`, which points to your organization's repository.

        ```
        git remote -v
        ```
        You should see something like this (with YOUR_ACCOUNT and
        CLASS_ORGANIZATION replaced by actual values).

        ```

        $ git remote -v
        origin    https://github.com/YOUR_ACCOUNT/make-me-laugh.git (fetch)
        origin    https://github.com/YOUR_ACCOUNT/make-me-laugh.git (push)
        upstream  https://github.com/CLASS_ORGANIZATION/make-me-laugh.git (fetch)
        upstream  https://github.com/CLASS_ORGANIZATION/make-me-laugh.git (push)
        ```
    Congratulations, your local clone now knows where to find the upstream repository (i.e., your organization's repository).

4. You will do some work in this repository. In the terminal window,

    1. Create a new file named `something_funny` that contains anything that
     you think is funny.

    2. Stage the file using

        ```
        git add something_funny
        ```

    3. Commit the changes using

        ```
        git commit -m "Created my own funny file"
        ```

    4. Push the changes to your fork:

       ```
       git push origin master
       ```

    Congratulations! You just created your own distinct fork of this repository.

5. __Do not proceed until your instructor tells you that you can, because something is about to
   change in the original (upstream) repository.__


6. Before you create another file, you need to pull down changes that were made after
   you forked and cloned the original.

    1. Pull down the master branch from the upstream:

       ```
       git pull upstream master
       ```

    2. What  Git command can show you the current state of the repository after this command?
       If you enter `ls` on the command line, you should see two more files in
      the working directory that are also in the repository. What are their names?

    3. Edit the file containing quotes from Dan Quayle by adding a new first line
       that states that Dan Quayle was George H. W. Bush's vice president.

    4. Stage and commit those changes as above.

    5. Push the resulting repository to your fork, as in step 4, substep iv above.

7. You have finished this activity. This is just a small taste of a simple
  workflow using Git.
