# Test File

**Initial Setup**

- [x] 1. Read the TOP contribuiting guide for the project.
- [x] 2. Nvigaet to the curriculum repository and fork the original ("upstream") repository into your own GitHub account by using the "fork" button at the top of that repo's page on GitHub.
- [x] 3. Clone your forked repository onto your local machine using something like git clone `git@github.com:your_user_name_here/curriculum.git` (you can get the url from the little widget on the sidebar on the right of that repo’s page on GitHub).
- [x] 4. Because you cloned the repository, you’ve already got a remote that points to `origin`, which is your fork on GitHub. You will use this to push changes back up to GitHub. You’ll also want to be able to pull directly from the original repository on GitHub, which we’ll call `upstream`, by setting it up as another remote. Do this by using the git command below inside the project folder `curriculum`:

```
git remote add upstream git@github.com:TheOdinProject/curriculum.git
```

**Ongoing workflow**
We’ve got one main branch – `main`. `main` is for production-ready code. Any code deployed to `main` (on the original repo, not on your fork) will be tested in staging and shipped to production. You’ll be working in a feature branch and submitting your pull requests to the `main` branch.

- [x] 1. Create a new feature branch for whatever feature you want to build, and add commits.
- [x] 2. When you’re done with your feature, odds are that someone has made changes to the upstream repository in the meantime. That means that your `main` branch is probably out of date. Fetch the most updated copy using `git fetch upstream`.
- [x] 3. Now merge the upstream’s changes into your local version of `main` using `git merge`. Specifically, you’ll first want to make sure you’re on your `main` branch using `git checkout main` and then `git merge upstream/main` to merge in those upstream changes that we just fetched.
- [x] 4. Now that your `main `branch is up-to-date with upstream, you need to merge it into your feature branch. Yes, that is correct and it seems odd at first. Don’t you want to merge the feature branch into the `main` branch instead? Yes, you do, but not yet. Your feature branch is dirty. You don’t know if it has any conflicts which might creep up. Any time you are merging in more “senior” branches (e.g. merging the feature into `main`), you want it to be a clean and conflict-free merge if possible. So you first merge the “senior” branch into your dirty branch to resolve those conflicts. Run `git checkout your_feature_name` to jump back onto your feature branch, then `git merge main` to merge `main` into it.
- [x] 5.You may have merge conflicts… resolve those using the skills you learned

**Sending your pull request**

- [x] 1. Now that your feature branch is squeaky clean and you know it’ll merge cleanly into `main`, the hard part is all over. All that’s left is to make the Pull Request (often abbreviated as PR) against our `upstream` repo on GitHub!
- [x] 2. Now you want to send your feature branch back up to your `origin` (your fork of the `upstream` repository). You can’t send directly to `upstream` because you don’t have access, so you’ll need to make a pull request. Use `git push origin your_feature_name` to ship your feature branch up to your fork on GitHub.
- [x] 3. If you have been following along with the above steps to get familiar with this workflow, **you should stop at this point**. If you have completed an assigned issue, the final step is to submit a pull request to merge your feature branch into the original `upstream` repository’s `main` branch. This can be done using GitHub’s interface.
- [x] Shake your moneymaker, you're an OSS contributor!
