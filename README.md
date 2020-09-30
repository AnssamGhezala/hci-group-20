## Prerequisites

- Node (v8.2.0 or higher)
- [Gatsby CLI](https://www.gatsbyjs.org/docs/)
- [Netlify CLI](https://github.com/netlify/cli)

### Access Locally

Pull this repository
```
$ git clone https://github.com/[GITHUB_USERNAME]/[REPO_NAME].git
$ cd [REPO_NAME]
$ npm install
$ npm install -g gatsby-cli netlify-cli
```

### Basics
#### Development mode
```
$ gatsby develop
```
Click on the localhost link and you'll see the website. After saving changes should be shown real time to your localhost port (should be localhost:8000).

#### Testing how the site will look when it's going to be live
##### Method 1: Testing it locally (recommanded)
```
$ gatsby build --prefix-paths
$ gatsby serve --prefix-paths
```
<br> The build command compiles your site and generates a new `public/` folder which is essentially our website but all the HTML, CSS and JavaScript files are optimized. Essentially that `public/` is our production build. 
<br> The serve command just hosts your production build into a localhost port (should be localhost:9000). Using this, you will be able to test your site as if it were LIVE.
##### Method 1: Testing it remotely on Netlify
Since this repository is linked to Netlify, everytime we push in the master branch, the site is deployed [here](https://hci-group-20.netlify.app/). So you can just click on the link and test your changes there.

#### Putting our site live
If you have not done this already, we have to first generate the `public/` folder with our latest changes by doing
```
$ gatsby build --prefix-paths
```
Then we move **the contents of** `public/` folder into the _www/hci/notebook_ directory in Anssam's ECE unix machine. I wonder if there's a way to make that directory into a git one then make a pipeline that takes care of updating the _www/hci/notebook_ directory_ everytime say we push to this repository.