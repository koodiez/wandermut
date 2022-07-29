# This is a guid to setup a development enviroment using this template

## Software you need to have installed

- [ ] [Shopify Themekit](https://shopify.dev/tools/theme-kit/getting-started)
- [ ] node & [npm](https://www.npmjs.com/get-npm)
- [ ] It's recommended to install extensions like Prettier
* If you don't want to use the git commands, you can use the inbuild git interface in your code editor or use external software such as [Sourcetree](https://www.sourcetreeapp.com/) or [Github Desktop](https://desktop.github.com/)

## Shop access you need from your customer

- [ ] Access to the store
- [ ] Being able to create a private app or get credentials for one they've created for you
  * When setting this up, the private app only needs read/write access for the theme nothing else

## Setup the environment

- [ ] Create a new repository using this template
- [ ] `git clone` the repository to your machine
- [ ] use `npm install` to install all dependencies
- [ ] duplicate the Live Theme
- [ ] create a private app
- [ ] duplicate the `config.example.yml` and change the name to `config.yml`
- [ ] Enter Store details (enter the ID for your new Development Theme)
- [ ] use `theme get` to download the status quo
- [ ] commit all files using your git tool or the command line with `git add .` & `git commit -m "Shopify status quo"`
- [ ] load the `bundle.css` in the `theme.liquid` by adding `<link rel="stylesheet" href="{{ 'bundle.css' | asset_url }}">` to the file

## How to develop

* **Never develop on the master branch**
* Before starting a new feature or bug, make sure to go to the master branch and use `git pull` to receive  all new changes
* Then use branches with names like `feature/{feature-name}` or `bugfix/{bugfix-name}` (Branches should always be created from the `master` branch)
* Use `npm run dev` to run `theme watch` and `webpack`
* SCSS/CSS changes need to be imported into the `src/styles.scss` using the `@use './folder/subfolder/filename.scss';` command (more [here](https://sass-lang.com/documentation/at-rules/use))
* Make sure to `commit` and `push` your git changes to the Github repository
  * Split-up big changes into multiple smaller commits to make it more readable

## How to deploy changes
* After you've pushed your changes from your feature  or bugfix branch, you can create a pull request
  * Make sure to write down what you wanted to change (What the outcome should look like on the page)
  * Small summary of what you've changed
* You're code will be reviewed, changes may be requested and when everything is resolved, merged to the `master` branch
* The person who reviewed and merged your code will then publish all new changes to the Live Theme


Work in progress, this guide is continuously updated.