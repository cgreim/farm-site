# Running and developing Farm Site

## Running Farm Site for the first time
Farm site is a Jekyll website project for Corner Farm Chicago. To run and develop it locally, you’ll need to [install Jekyll](https://jekyllrb.com/docs/installation/). Farm site also uses Ruby 2.4.0.
Once installed, clone the repository by clicking the green “Clone or download” button and copying the link. In Terminal, navigate to where you want to keep the directory, and type:
```shell
git clone https://github.com/cgreim/farm-site.git
```
_If you're using SSH instead of HTTP, replace the above with the SSH link instead._


## Running Farm Site on-going
To run farm site, first open Terminal. Navigate to where your farm site directory is with `cd`, eg:
```shell
cd sites/farm-site
```
where `sites/` is the path to farm-site.
Once inside farm-site, make sure you’re on the correct branch. It’s a good idea to sync with GitHub and make sure you’re using the latest updates to our production branch, `master`, so let’s start by typing:
```shell
git checkout master
git fetch
git pull
```
- `git checkout master` switched us into the master branch. Right now, anything merged into `master` will be live, viewable to anyone at [cgreim.github.io/farm-site](https://cgreim.github.io/farm-site/).
- `git fetch` had our computer check-in with GitHub. It might have returned some lines like this:
  ```shell
  From https://github.com/cgreim/farm-site
   * [new branch]      bootstrap-cdn -> origin/bootstrap-cdn
  ```
  It’s important to note that `git fetch` _doesn’t pull those changes locally to your computer._ It just lets you see that changes have been made. To sync the changes locally, you need:
- `git pull` pulls updates down from GitHub. Now that we’re all synced, we’re ready to run farm site locally.

Next, in command line type:
```shell
bundle exec jekyll serve
```
This command starts jekyll running and compiling. You can see your compiled site by visiting `http://localhost:4000/` in your browser. While jekyll is running, it will update your site locally with any changes you make to the code, and it will let you know if there are any compilation errors. When you’re ready to quit, type `ctrl + c` in terminal.
