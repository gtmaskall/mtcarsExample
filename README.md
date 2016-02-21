# Illustrating gh-pages branch for publishing

## Introduction

Okay, so you've done a great little analysis and are pushing it to 
your github repo. Fine. But wait, your output is an html file
with really cool and colourful plots etc. and in your github
repo it only appears as a plain old html source file. What you
really want is to push it to github.io where people can view
it for the proper web page it is.

## Steps

### Setting up

First, I'm going to create the repo locally and push my lovely, 
amazing analysis to github. I've initialized the repo locally
already, so just want to create an empty github repo.

1. cd to my source directory
2. initialize the repo: `git init`
3. add my files: `git add .`
    * your exact commands may vary as you iterately add files,
but we expect you to know the basics of adding files to
git by now
4. commit the files: `git commit`, and
5. add the remote repository: `git remote add origin https://github.com/blah/something.git`
5. push to github: `git push -u origin master`

So now, you've got your files safely up on github. But, erm, weren't
we talking about publishing your html report? NB: we're assuming the
above files actually included such an html report!

### Publishing your magnus opus

Okay, so far we've basically done nothing more than get to the point
where we have stuff locally in a git repo and on github.
This is really because you probably already have an existing repo.
Otherwise, you could actually have just gone straight to creating the branch
as in the next sequence.

Next, simply:

1. go to your github repo on the web
2. click on the "Branch" button (it should be saying "master" right now)
3. type "gh-pages" into the "Find or create a branch" box,
4. select to create the branch
5. You should now be done

I then verified, by doing:

1. in your local repo, execute `git checkout -b gh-pages`
2. you should then get a response `Switched to a new branch 'gh-pages'`
3. if you then run `git push origin gh-pages`, you should get `Everything up-to-date`
4. other useful checks are:
    * `git remote -v`
    * and `git status` - this particularly should confirm you're on your gh-pages branch

## URL

You know where this repo is on github, because you're reading the README.md file. So where's
this published file? It's [here](https://gtmaskall.github.io/mtcarsExample/mtcarsAnalysis.html).
Notice how the URL of the published document is built from your username, the name of your
repo, and then the name of your output html file.

## Summary

In short:

* Create a gh-pages branch containing your compiled rmarkdown report
* Publish the URL from github.io! `https://username.github.io/reponame/report.html`
