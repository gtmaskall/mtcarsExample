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
  your exact commands may vary as you iterately add files,
but we expect you to know the basics of adding files to
git by now
4. commit the files: `git commit`, and
5. add the remote repository: `git remote add origin https://github.com/blah/something.git`
5. push to github: `git push -u origin master`

So now, you've got your files safely up on github. But, erm, weren't
we talking about publishing your html report? NB: we're assuming the
above files actually included such an html report!
