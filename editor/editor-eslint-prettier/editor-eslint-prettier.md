# ESLint + Prettier 

### Install
```bash
$ npm i - D eslint
```
### Install the Prettier formatter dependencies.
```bash
$ npm i -D prettier eslint-config-prettier eslint-plugin-prettier
```
### Create a file for the ESLint configuration (.eslintrc.json) to add the Prettier rules.
```
{
  "extends": ["prettier"],
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": [
      "error",
      {
        "singleQuote": true
      }
    ]
  }
}
```
### Configure the VS Code so that only the ESLint extension formats the code.
```
{
  // enable format on save.
  "editor.formatOnSave": true,
  // configure the actions that should be performed when saving a file.
  "editor.codeActionsOnSave": {
    // run ESLint
    "source.fixAll.eslint": true
  },
  // disable the Prettier plugin for .js and .jsx files.
  "prettier.disableLanguages": ["javascript", "javascriptreact"]
}
```