# CodeLab

## Part 1: VSCode

1. Install **Prettier** plugin

<img align="center" src="img/s1.png">

2. Install **Eslint** plugin

<img align="center" src="img/s2.png">

## Part 2: Eslint

1. Open your package.json, go down there on the **eslintConfig** and leave it as the next is:

   ```json
   "eslintConfig": {
   	"extends": [
   		"eslint:recommended",
   		"react-app",
   		"react-app/jest",
   		"prettier"
   	]
   },
   ```

   <img align="center" src="img/s3.png">

2. run **_npm i -D eslint_**
   <img align="center" src="img/s4.png">
3. add this 2 new scripts to the **package.json**
   ```json
   "lint": "eslint --ext .js,.jsx .",
   "lint:fix": "npm run lint -- --fix"
   ```
   <img align="center" src="img/s5.png">

## Part 3: Prettier

1. go to your package.json
2. add a new key down below **eslintConfig**, like this:

   ```json
   "prettier": {}
   ```

   <img align="center" src="img/s6.png">

3. Go to **_file/preferences/settings_** another alternative is pressing on windows **ctrl + ,**
4. On the User configuration open **_Text Editor / Formatting_**
5. Click on **Format On Save** checkbox.

<img align="center" src="img/s7.png">

## Part 4: Husky

1. run **_npm i -D husky_**

<img align="center" src="img/s8.png">

2. run **_npm set-script prepare "husky install"_**
3. run **_npm run prepare_**
4. run **_npm i -D prettier_**

<img align="center" src="img/s9.png">

5. run **_npm set-script format "prettier --write ."_**
6. run **_npx husky add .husky/pre-commit "npm run lint:fix && npm format"_**

<img align="center" src="img/s10.png">

## Author

- Kristhian David Segura
