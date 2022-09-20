# www.stephenbaek.com

This repository contains the source code of Stephen Baek's personal website (http://www.stephenbaek.com). I'm using this awesome template called [Tale](https://github.com/chesterhow/tale), and most of the credits for the graphic design, layouts, and such should be directed to [@chesterhow](https://github.com/chesterhow), the original creator of the template. (If that's the reason why you are checking out this repo, I encourage you to visit the original repo for more details.)

## How to Contribute
If you are here to contribute to the website, you must be one of my friends, colleagues, students, etc.--as a matter of fact, a significant number of pages on my website is designated for works resulting from collaborating with my dear friends and colleagues. Or maybe you are a complete stranger! (I don't know why would a random stranger be willing to contribute to my personal page, but hey, the internet is a weird place!) In any case, your contributions are always welcome! Below are some guidelines to assist you.

### Issues (Direct Collaborators & Public)
The easiest way of making contribution is through posting suggestions, requests, questions, etc. on the "[Issues](https://github.com/stephenbaek/stephenbaek.github.io/issues)" tab. There must be "New issue" button on the top right corner. Simply go ahead and hit the button, and leave comments.

I ask you to be as specific as possible, so that I can address your issue promptly and thoroughly. There's no specific format or template, and you can feel free to leave comments as you see fit. Hyperlinks, screenshots, examples, minimum working codes, and such are always encouraged, as they would give me a better understanding.

While this might be the simplest way for you to contribute, this could also be the slowest way. I only work on this website every once in a while, and reviewing issues myself and making changes accordingly may take some time. If you are looking for a quicker update, you may also want to consider the alternative method below.


### Pull Requests via Web Browser (Direct Collaborators Only)
Pull requests are, in fact, much preferred way of making contributions, because they are specific, contain explicit/direct edits, and overall are easy to adopt. If you are one of **my student colleagues and/or from my research team**, I strongly encourage you to use this method to make contributions.

The first thing to do to make a contribution in this way is to create a GitHub account and emailing me the account info so that I can add you as a collaborator. Once you are added to the repo as a collaborator, you will be able to create new *branches* [here](https://github.com/stephenbaek/stephenbaek.github.io/branches). In case you are not familiar with GitHub, "branches" are essentially different "versions" of the code base. I ask you to create your own branch each time you make a contribution so that I can keep track of different versions of the code and make sure there are not any conflicting changes being made by multiple contributors. That said, you should NEVER touch the `master` branch, since `master` is where the "camera-ready" version stays that is used to render the actual website.

Once you've created a branch, please then make changes directly to the branch. If you are new to GitHub, it offers an web interface to edit the codes, which might probably the easiest option for you. On the web interface, first, to make sure your changes take place in the new branch, click the dropdown list on the left top corner next to 'XX branches,' 'XX tags' icon (see the screenshot below).
![](/assets/docs/branch_selection.png)

Once you are in the branch you created, now navigate to the location of the page you would like to modify. In terms of how folders and files are structured, I'll try to explain things more clearly. For now, let's assume that you intend to make changes to the MaterIQ project page, which is located under `projects/materiq/materiq.md`. When you click the file, you will see the preview of the page as in this screenshot:
![](/assets/docs/page_preview.png)

Right above the preview, there should be a little "pencil" button you can click. To edit the page, go ahead and click the pencil button, which will open up an online text editor like the screenshot below. In the editor, you can make changes you intended to make. It gives you a preview of how things are going to be rendered, so it's always a good idea to check the preview frequently to make sure that the page is rendered in a way you intended. Note that most of the pages on the website are written in the [Markdown language](https://www.markdownguide.org/) and [HTML](https://www.w3schools.com/html/html_intro.asp). Even if you are not familiar with those languages, the syntax should be straightforward for most of the part. So don't be afraid of making changes in the text editor. Even if you break something, it will not damage or burn down the actual website---that's the whole point of using branches!
![](/assets/docs/page_edit.png)

Once you are done with editing the page, you can go ahead and *commit* those changes. Committing changes basically mean that you'd like to save the result in the repository. Once you commit, the changes become available to the others. Of course, you can commit changes however frequently you'd like. Just remember that once you commit changes, all the things you've done will become official. So, it'd be a good idea to check everything is good to go before committing the changes. 'Commit changes' button is available at the bottom of the text editor. As you can see in the screenshot below, each commit must have a short description of the changes being made. Please try to provide a short but useful description of your changes. Once you are done, go ahead and hit the button.
![](/assets/docs/commit.png)

After making all the commits (or just a single commit) you want to make, you may feel those changes are ready to be merged to the running website. Remember, those commits you make on your branch are just temporary versions of the website, that is not visible to the visitors of the website. Therefore, to make those changes finally official, you need to make one last step, called "pull request". To make a pull request, what you need to do is to go to the "Pull requests" tab and hit "New pull request" or "Compare & pull request" button (see the screenshot below). 
![](/assets/docs/new_pull_request.png)

This will lead you to "Open a pull request" screen (below), in which you can describe the changes you've made and request those changes be reflected to the website. Usually, there's nothing much you need to do but just clicking "Create pull request" button should be enough. Perhaps leave some comments describing what kind of contributions you've made before submitting the pull request, which is optional.
![](/assets/docs/pull_request.png)

Okay, that's all you need to do to contribute to the website. Now, just to give you an idea of what the next process looks like (on my end), once your pull request comes in, I'll be able to see what kind of (final) changes you've made (something like the screenshot below) and I can decide whether or not to merge those changes into the master branch to reflect them onto the actual website. If necessary, I can add/edit/discard your changes as well. So again, don't worry of "burning down the house." :)
![](/assets/docs/merge.png)



### Pull Requests via Git (Direct Collaborators Only)
(Instructions will be added here.)
#### Ruby and Bundle Install
#### Jekyll Serve
