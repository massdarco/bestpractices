**Setting Up a Linter**

- Install ESLint globally - optional

    `sudo npm install -g eslint`

- VS Code ESLint extension

    - Launch VS Code Quick Open `(Ctrl+P)`, paste the following command, and press enter.
    
        `ext install dbaeumer.vscode-eslint`

- install devDependencies packages

    `npm i -D eslint eslint-config-airbnb-base eslint-config-node eslint-config-prettier eslint-plugin-node eslint-plugin-prettier prettier`

- create `.eslintrc.json` and insert json below

``` json
{
    "env": {
        "commonjs": true,
        "es6": true,
        "node": true
    },
    "extends": ["airbnb-base", "plugin:prettier/recommended"],
    "globals": {
        "Atomics": "readonly",
        "SharedArrayBuffer": "readonly"
    },
    "parserOptions": {
        "ecmaVersion": 2018
    },
    "rules": {
        "prettier/prettier": ["error"]
    },
    "plugins": ["prettier"]
}
```
- optional can ignore file from eslint by create `.eslintignore` file and add file path like

    `bin/www`

- create `.prettierrc` and insert code below

``` json
{
    "printWidth": 100,
    "singleQuote": true
  }
```
