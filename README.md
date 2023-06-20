# configure_prettier



1. https://itnext.io/configure-prettier-and-eslint-with-angular-e7b4ce979cd8
2. https://www.youtube.com/watch?v=wtJeWrDmZ5A

Steps to follow :

1- ng add @angular-eslint/schematics

2- ng lint --fix

3- npm install prettier --save-dev

4 - Then we need to add .prettierrc.json and .prettierignore files in our root project directory.

5- npx prettier --write

6 - Inside .prettierrc.json we can change the default settings by overriding them.

The settings I use most of the time are this:

{
  "tabWidth": 2,
  "useTabs": false,
  "singleQuote": true,
  "semi": true,
  "bracketSpacing": true,
  "arrowParens": "avoid",
  "trailingComma": "es5",
  "bracketSameLine": true,
  "printWidth": 80
}

7- npm install prettier-eslint eslint-config-prettier eslint-plugin-prettier --save-dev


8- in .eslintrc.json

    {
      "files": ["*.ts"],
      "extends": [
        ...
        "plugin:prettier/recommended" // put this line
      ],
    },

  
