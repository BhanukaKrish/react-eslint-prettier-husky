# Create React App

### `npx create-react-app react-eslint-prettier-husky`

<!-- ### `npm install --save-dev eslint prettier eslint-config-prettier eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks husky lint-staged` -->

# Install ESLint

### `npm install eslint --save-dev`

# Install ESLint Config

### `npm init @eslint/config`

you will need to answer some questions about how you would like to use eslint follow the following configuration
(note that I chose react as the library, Airbnb as the style guide, and JSON as the file format. You can change these configurations according to your project)

that object of rules:{} is where you can put your own rules if you want to but for now, we are using Airbnb rules as mentioned in "extends": ["plugin:react/recommended", "airbnb"]
For more on eslint rules you can check their official site [https://eslint.org/docs/latest/rules/](https://eslint.org/docs/latest/rules/)

# Install Prettier

### `npm install --save-dev --save-exact prettier`

in the root folder create a file named .prettierrc.json this will contain custom rules/options that you may want prettier to follow while formatting your code. enter the following code in your .prettierrc.json

```
{
"tabWidth": 2,
"useTabs": true,
"printWidth": 80,
"semi": true,
"trailingComma": "es5",
"singleQuote": true,
"endOfLine": "lf"
}
```
you can learn more about these prettier rules and more on their official site [https://prettier.io/docs/en/options.html](https://prettier.io/docs/en/options.html)

# Integrating Prettier with ESLint

### `npm install --save-dev eslint-config-prettier`

to configure eslint-config-prettier in your .eslintrc.json extent "prettier" add it as last like following

```
"extends": ["plugin:react/recommended", "airbnb", "prettier"],
```

# Configure scripts

```
"scripts": {
... // other scripts you have
"lint": "eslint . --fix --max-warnings=0"
"format": "prettier . --write"
},
```

"lint": "eslint . --fix --max-warnings=0": this script runs eslint from the root folder and auto fix error and checks that we don't have any warning
"format": "prettier . --write": this script will run prettier from the root folder and auto fix format errors

# Install Husky

