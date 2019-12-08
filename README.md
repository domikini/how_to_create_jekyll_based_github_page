# How to create a Jekyll based github page
Original text:
https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#creating-your-site

[GitHub Help](https://help.github.com/en)

-   [GitHub.com](https://help.github.com/en/github)
-   [Enterprise Server](https://help.github.com/en/enterprise/admin)
-   [GitHub Actions](https://help.github.com/en/actions)
-   [GitHub Desktop](https://help.github.com/en/desktop)
-   [Atom](https://atom.io/docs)
-   [Electron](https://electronjs.org/docs)

English

Article version: GitHub.com

[GitHub.com](https://help.github.com/en/github "product: GitHub.com")  [GitHub Pages](https://help.github.com/en/github/working-with-github-pages "guide: GitHub Pages")  [Setting up a GitHub Pages site with Jekyll](https://help.github.com/en/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll "topic: Setting up a GitHub Pages site with Jekyll")  [Creating a GitHub Pages site with Jekyll](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll "article: Creating a GitHub Pages site with Jekyll")

# Creating a GitHub Pages site with Jekyll

You can use Jekyll to create a GitHub Pages site in a new or existing repository.

[Mac](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#)[Windows](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#)[Linux](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#)[All](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#)

GitHub Pages is available in public repositories with GitHub Free, and in public and private repositories with GitHub Pro, GitHub Team, GitHub Enterprise Cloud, and GitHub Enterprise Server. For more information, see "[GitHub's products](https://help.github.com/articles/github-s-products)."

People with admin permissions for a repository can create a GitHub Pages site with Jekyll.

### [In this article](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#in-this-article)

-   [Prerequisites](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#prerequisites)
-   [Creating a repository for your site](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#creating-a-repository-for-your-site)
-   [Creating your site](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#creating-your-site)
-   [Next steps](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#next-steps)

### [Prerequisites](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#prerequisites)

Before you can use Jekyll to create a GitHub Pages site, you must install Jekyll and Git. For more information, see  [Installation](https://jekyllrb.com/docs/installation/)  in the Jekyll documentation and "[Set up Git](https://help.github.com/en/articles/set-up-git)."

We recommend using  [Bundler](http://bundler.io/)  to install and run Jekyll. Bundler manages Ruby gem dependencies, reduces Jekyll build errors, and prevents environment-related bugs. To install Bundler:

1.  Install Ruby. For more information, see "[Installing Ruby](https://www.ruby-lang.org/en/documentation/installation/)" in the Ruby documentation.
2.  Install Bundler. For more information, see "[Bundler](https://bundler.io/)."

### [Creating a repository for your site](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#creating-a-repository-for-your-site)

If your site is an independent project, you can create a new repository to store your site's source code. If your site is associated with an existing project, you can add the source code for your site to a  `gh-pages`  branch or a  `docs`  folder on the  `master`  branch in that project's repository. For example, if you're creating a site to publish documentation for a project that's already on GitHub, you may want to store the source code for the site in the same repository as the project.

If you want to create a site in an existing repository, skip to the "[Creating your site](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#creating-your-site)" section.

**Warning**: GitHub Pages sites are publicly available on the internet, even if their repositories are private. If you have sensitive data in your site's repository, you may want to remove it before publishing.

1.  In the upper-right corner of any page, use the  drop-down menu, and select  **New repository**.
    
    ![Drop-down with option to create a new repository](https://help.github.com/assets/images/help/repository/repo-create.png)
    
2.  Use the  **Owner**  drop-down menu, and select the account you want to own the repository.
    
    ![Owner drop-down menu](https://help.github.com/assets/images/help/repository/create-repository-owner.png)
    
3.  Type a name for your repository and an optional description. If you're creating a user or organization site, your repository must be named  `<user>.github.io`  or  `<organization>.github.io`. For more information, see "[About GitHub Pages](https://help.github.com/en/articles/about-github-pages#types-of-github-pages-sites)."
    
    ![Create repository field](https://help.github.com/assets/images/help/pages/create-repository-name-pages.png)
    
4.  Choose to make the repository either public or private. Public repositories are visible to the public, while private repositories are only accessible to you, and people you share them with. For more information, see "[Setting repository visibility](https://help.github.com/en/articles/setting-repository-visibility)."
    
    ![Radio buttons to select private or public status](https://help.github.com/assets/images/help/repository/create-repository-public-private.png)
    

### [Creating your site](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#creating-your-site)

Before you can create your site, you must have a repository for your site on GitHub. If you're not creating your site in an existing repository, see "[Creating a repository for your site](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#creating-a-repository-for-your-site)."

1.  Open  Git Bash.
    
2.  If you don't already have a local copy of your repository, navigate to the location where you want to store your site's source files, replacing  _PARENT-FOLDER_  with the folder you want to contain the folder for your repository.
    
    ```shell
    $ cd PARENT-FOLDER
    ```
    
3.  If you haven't already, initialize a local Git repository, replacing  _REPOSITORY-NAME_  with the name of your repository.
    
    ```shell
    $ git init REPOSITORY-NAME
    > Initialized empty Git repository in /Users/octocat/my-site/.git/
    # Creates a new folder on your computer, initialized as a Git repository
    ```
    
4.  Change directories to the repository.
    
    ```shell
    $ cd REPOSITORY-NAME
    # Changes the working directory
    ```
    
5.  If you're creating a project site, decide which publishing source you want to use. If you're creating a user or organization site, you must store your site's source code on the  `master`  branch. For more information, see "[About GitHub Pages](https://help.github.com/en/articles/about-github-pages#publishing-sources-for-github-pages-sites)."
    
6.  Navigate to the publishing source for your site. For more information about publishing sources, see "[About GitHub Pages](https://help.github.com/en/articles/about-github-pages#publishing-sources-for-github-pages-sites)."
    
    For example, if you chose to publish your site from the  `docs`  folder on the  `master`  branch, create and change directories to the  `docs`  folder.
    
    ```shell
    $ mkdir docs
    # Creates a new folder called docs
    $ cd docs
    ```
    
    If you chose to publish your site from the  `gh-pages`  branch, create and checkout the  `gh-pages`  branch.
    
    ```shell
    $ git checkout --orphan gh-pages
    # Creates a new branch, with no history or contents, called gh-pages and switches to the gh-pages branch
    ```
    
7.  To create a new Jekyll site, use the  `jekyll new`  command, replacing  _VERSION_  with the current dependency version for Jekyll. For more information, see "[Dependency versions](https://pages.github.com/versions/)" on the GitHub Pages site.
    
    -   If you installed Bundler:
        
        ```shell
        $ bundle exec jekyll VERSION new .
        # Creates a Jekyll site in the current directory
        ```
        
    -   If you don't have Bundler installed:
        
        ```shell
        $ jekyll VERSION new .
        # Creates a Jekyll site in the current directory
        ```
        
8.  Open the Gemfile that was created and follow the instructions in the Gemfile's comments to use GitHub Pages.
    
    ![Instructions for updating Gemfile](https://help.github.com/assets/images/help/pages/gemfile-instructions.png)
    
9.  Update the  `gem "github-pages"`  line so that the line looks like this, replacing  _VERSION_  with the current dependency version for  `github-pages`. For more information, see "[Dependency versions](https://pages.github.com/versions/)" on the GitHub Pages site.
    
    ```shell
    gem "github-pages", "~> VERSION", group: :jekyll_plugins
    ```
    
10.  Save and close the Gemfile.
    
11.  Optionally, test your site locally. For more information, see "[Testing your GitHub Pages site locally with Jekyll](https://help.github.com/en/articles/testing-your-github-pages-site-locally-with-jekyll)."
    
12.  Add your GitHub repository as a remote, replacing  _USER_  with the account that owns the repository and  _REPOSITORY_  with the name of the repository.
    
    ```shell
    $ git remote add origin https://github.com/USER/REPOSITORY.git
    
    ```
    
13.  Push the repository to GitHub, replacing  _BRANCH_  with the name of the branch you're working on.
    
    ```shell
    $ git push -u origin BRANCH
    ```
    
14.  If you're using a non-default publishing source for a project site, configure your publishing source. For more information, see "[Configuring a publishing source for your GitHub Pages site](https://help.github.com/en/articles/configuring-a-publishing-source-for-your-github-pages-site#choosing-a-publishing-source)."
    
15.  On GitHub, navigate to your site's repository.
    
16.  Under your repository name, click  **Settings**.
    
    ![Repository settings button](https://help.github.com/assets/images/help/repository/repo-actions-settings.png)
    
17.  To see your published site, under "GitHub Pages", click your site's URL.
    
    ![URL of your published site](https://help.github.com/assets/images/help/pages/click-pages-url-to-preview.png)
    
    **Note:**  It can take up to 20 minutes for changes to your site to publish after you push the changes to GitHub. If your don't see your changes reflected in your browser after an hour, see "[About Jekyll build errors for GitHub Pages sites](https://help.github.com/en/articles/about-jekyll-build-errors-for-github-pages-sites)."
    

**Note**: If your site's source files are located in the default publishing source—`master`  for user and organization sites or  `gh-pages`  for project sites—but your site has not published automatically, make sure someone with admin permissions and a verified email address has pushed to the default publishing source.

### [Next steps](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll#next-steps)

To add a new page or post to your site, see "[Adding content to your GitHub Pages site using Jekyll](https://help.github.com/en/articles/adding-content-to-your-github-pages-site-using-jekyll)."

You can add a Jekyll theme to your GitHub Pages site to customize the look and feel of your site. For more information, see "[Adding a theme to your GitHub Pages site using Jekyll](https://help.github.com/en/articles/adding-a-theme-to-your-github-pages-site-using-jekyll)."

### Ask a human

#### Can't find what you're looking for?

[Contact us](https://support.github.com/contact)

#### Product

-   [Features](https://github.com/features)
-   [Security](https://github.com/security)
-   [Enterprise](https://github.com/enterprise)
-   [Case Studies](https://github.com/case-studies?type=customers)
-   [Pricing](https://github.com/pricing)
-   [Resources](https://resources.github.com/)

#### Platform

-   [Developer API](https://developer.github.com/)
-   [Partners](http://partner.github.com/)
-   [Atom](https://atom.io/)
-   [Electron](http://electron.atom.io/)
-   [GitHub Desktop](https://desktop.github.com/)

#### Support

-   [Help](https://help.github.com/)
-   [Community Forum](https://github.community/)
-   [Training](https://services.github.com/)
-   [Status](https://githubstatus.com/)
-   [Contact GitHub](https://support.github.com/contact)

#### Company

-   [About](https://github.com/about)
-   [Blog](https://github.blog/)
-   [Careers](https://github.com/about/careers)
-   [Press](https://github.com/about/press)
-   [Shop](https://shop.github.com/)

-   © 2019 GitHub, Inc.
-   [Terms](https://help.github.com/articles/github-terms-of-service/)
-   [Privacy](https://help.github.com/articles/github-privacy-statement/)
