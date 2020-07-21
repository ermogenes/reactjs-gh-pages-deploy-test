# reactjs-gh-pages-deploy-test
Repository created to test deploy of a ReactJs app on GitHub Pages

## 1. Create a GitHub repository

URL will be `http://<username>.github.io/<repo-name>`.

You may create a `README.md`.

## 2. Clone the repo

## 3. Create an empty React app inside

The name of the app doesn't need to be the same of the repo.

```
create-react-app reactjs-gh-pages-deploy-test
```

## 4. Install `gh-pages` as a dev-dependency

Do it on the app folder, not in root.

```
yarn add gh-pages -D
```

## 5. Edit `package.json`

Add this (with you user and repo names):

```json
  //...
  "homepage": "http://<username>.github.io/<repo-name>",
  //...
```

And this:

```json
//...
"scripts": {
  //...
  "predeploy": "yarn build",
  "deploy": "gh-pages -d build"
  //...
}
//...
```

## 6. Deploy!

Run:

```
yarn deploy
```

It will build your app on `build` folder and save it all on a branch named `gh-pages`. It will also commit, push and configure GitHub Pages!

Your source code is independent. Commit it at will. Your page will be updated only after a deploy.

## 7. Enjoy!

This repository was created with this procedure. See it [live](https://ermogenes.github.io/reactjs-gh-pages-deploy-test/).