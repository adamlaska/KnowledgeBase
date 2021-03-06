---
title: How to add a merchant to NavCoin.org
date: "2019-03-21"
---

### Create or Claim an issue
If you've found or heard of a new merchant that accepts NAV, create an issue on GitHub about adding them to the site. Or if have a look at the existing issues to see if there are any merchants requesting to be added.

https://github.com/NAVCoin/navcoin-org/issues

Make sure you create and/or claim an issue to avoid doubling up on work with someone else who is also trying to help maintain the website.

### Fork the repository

Login to GitHub and browse to the NavCoin.org repository.

https://github.com/NAVCoin/navcoin-org

Click the Fork button in the top right corner and it will clone the code for the website to your own GitHub account. Since the main NavCoin.org repository cant be committed to directly, you need to work on your own repo and then create a pull request which will be covered later.

### Clone the repository and create a branch

You can use either the Git command line or a GUI like GitKraken to clone your forked repository to you local computer and create a branch to make the changes in.


### Source and add the image for the merchant listing

The images for the merchant listing should be a 1:1 square ratio. The easiest place to find a good square cropped logo is usually the twitter profile picture for the merchant.  If you can't find a good square one, you might have to crop your own from their website logo using something like photoshop or an online cropping service like Croppola.

Once you have your image sourced, add it to the merchant images directory, ensuring it has a unique name. For this example, we will be adding a merchant called "Bobs Burgers".
```
/themes/nav-community-v2/static/images/merchants/bobs-burgers.jpg
```

### Add the listing to the merchants page

Open the mark down file for the english version of the merchants page.
```
/content/merchants/index.en.md
```
Copy and paste one of the merchant shortcode blocks and replace the content with the new merchants details, for example;
```
{{</* merchant
    titleText="Bobs Burgers"
    imgSrc="/images/merchants/bobs-burgers.jpg"
    text="Burgers that speak for themselves."
    linkUrl="https://bobsburgers.com"
*/>}}
```

You'll need to add this block of code to all of files found in this folder so it displays in all languages.

### Check it works

From the folder you cloned the site into, you can start up the site with the `hugo server` command in terminal. Then you should be able to preview the site on `https://localhost:1313`.

If you don't have hugo installed, check out https://gohugo.io for instructions on how to run it on your operating system.

### Push to GitHub and create the PR for review

Using Git CLI or GitKraken, commit the changes and push them back up to your GitHub fork. Then through GitHub create a pull request to merge your branch back into the original NavCoin.org repository's master branch. You should see the branch build and get a preview link to check it all works properly.

PR's require two positive reviews from collaborators before they can be merged. When you've submitted your PR for review, feel free to add some of the NavCoin core devs as reviewers and nudge them on Discord to review and merge it.
