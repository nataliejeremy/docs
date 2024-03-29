---
title: Starting With Git
parent_guide:
    - getting-started
filename: source/_docs/starting-with-git.md
---

Git is the version control tool at the heart of the Pantheon workflow. If you're a developer who likes to use local development, it's likely the best way to work with the Pantheon platform: develop locally, commit, and push to master to deploy code into your Pantheon development environment.

### Clone your site codebase

The first step is to get a `git clone` a of your code from Pantheon to your local computer.

#### Step 1: Go to your site dashboard

Log into Pantheon and load the dashboard page for the site you want to work on.

#### Step 2: Copy the Git Clone command

At the top of the development panel you will see the `git clone` command. It will look something like this:

![Copy Past Git Clone](https://pantheon-systems.desk.com/customer/portal/attachments/278869)

Copy and paste that to your terminal to get started.

#### Step 3: Run `git clone`

On your local environment go to where you want the code to reside. Git will create a directory as part of the clone, so you don't need to create one. Go ahead and run the command you copied in step 2:

    git clone ssh://codeserver.dev.xxx@codeserver.dev.xxx.drush.in:2222/~/repository.git my-site

If everything worked you should see Git fetching the data:

![Git Clone During](https://pantheon-systems.desk.com/customer/portal/attachments/27623)

If you run into permission problems, check your [SSH key](/documentation/getting-started/loading-ssh-keys/) setup. If the clone starts but can't complete, check your network and be sure your version of git is current.

### Make a change

#### Step 1: Edit a file

You can now edit your site code using any text editor. We recommend using [a butterfly](http://xkcd.com/378/).

#### Step 2: Add a file

If you want to add a new file to your codebase you will need to tell Git about it. Otherwise, Git will not track the file.

    git add _path_to_file_

To find out if you have any files in your local clone that git isn't yet tracking, try:

    git status

Any pending changes and files to be added will be listed like this:

![Git Status](https://pantheon-systems.desk.com/customer/portal/attachments/27626)

You can then cut and paste the paths to these files when using _git add_.

### Push Changes to Pantheon

Sending code to Pantheon is a two-step process with Git. First, you need to commit the files locally. Then you need to "push" them to the Pantheon cloud.

#### Step 1: Commit the files locally

In order to tell Git the files are ready, you need to commit them. Every commit includes a brief message to this commit so you can later remember why the change was made. It is worthwhile to take a moment and create a thoughtful commit message. Your colleagues (or even just your future self) will be thankful.

    git commit -am "Adding a great new module to increase awesomesauce level of my Drupal site."

If you don't specify a message on the command-line, git will open your default text-editor and prompt you to create one. Exiting without making a message will abort the commit. If the commit worked you will see something like this:

![Git Commit](https://pantheon-systems.desk.com/customer/portal/attachments/27624)

There is a handy list of git commands (along with a lot of other documentation) over [on GitHub](https://github.com/AlexZeitler/gitcheatsheet/blob/master/gitcheatsheet.pdf)

#### Step 2: Send the changes to Pantheon

You have committed the file locally, but you still need to send the changes to Pantheon. To do this you use the push command:

    git push origin master

This executes a "push" to the "origin" location, which is Pantheon since that's where you cloned the code from, on the branch "master", which is what your Dev environment tracks.

If you have a password on your SSH key, you may need to enter it to authorize the push. If everything worked, you will see something like this:

![Git Push](https://pantheon-systems.desk.com/customer/portal/attachments/27625)

#### Step 3: Check out the changes on Pantheon!

When the push command completes Pantheon instantly deploys the changes to your development server. It's time to check them out.

Go back to your site's dev tab in Pantheon and find the site sidebar. Click on the URL under "Development site" and browse to your changes.

### Wrapping up

Nice work, you are finished! You can now access your codebase on your computer, make changes, and deploy them to Pantheon.

For further learning, we recommend checking out the following resources:

- [Git Documentation](http://git-scm.com/documentation)
- [Pro Git Book](http://git-scm.com/book)
- [Git Reference](http://gitref.org/)
- [Git Cheatsheet](http://ndpsoftware.com/git-cheatsheet.html)
- [Git Immersion](http://gitimmersion.com/)
- [Code School - Try Git](http://try.github.io/levels/1/challenges/1)
- [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/)
- [SourceTree - Git GUI client](http://www.sourcetreeapp.com/)

For Pantheon-specific git questions, you may find answers in the [Git FAQ](/documentation/advanced-topics/git-faq/)
