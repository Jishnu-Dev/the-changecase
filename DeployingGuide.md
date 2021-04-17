URL to the guide:  https://dev.to/rolanddoda/deploy-to-github-pages-like-a-pro-with-github-actions-4hdg

1) For Vue create a new file in your project root named vue.config.js
    inside vue.config.js -> 

    module.exports = {
        publicPath: '/name-of-your-repo/'
    }

Now commit and push your changes.
Note: if you don't commit your changes, you will lose them in the next command, so make sure you don't skip this step

2) Open your terminal in your project and run:

    git checkout --orphan gh-pages Docs
    npm run build
    git --work-tree dist add --all Docs (for react: replace dist with build)
    git --work-tree dist commit -m 'Deploy' (for react: replace dist with build)
    git push origin HEAD:gh-pages --force
    rm -r dist (for react: replace dist with build)
    git checkout -f master
    git branch -D gh-pages

Navigate to your github project and click 'Settings'
Scroll to find the section 'Github Pages' , select the gh-pages branch and click 'Save'
Your site is ready to be published.