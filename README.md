# THIS IS ONLY A PERSONAL GUIDE.

* Task Runners são ferramentas que automatizam tarefas repetitivas no desenvolvimento web(NPM SCRIPTS). [executores de tarefas]

## §Linters:

### Linters são ferramentas que analisam o código-fonte em busca de erros, problemas de estilo e possíveis bugs. (ESLINT)

## §Formatters

### Formatters são ferramentas que ajustam automaticamente a formatação do código-fonte para garantir consistência e legibilidade. (PRETTIER)

## HOW TO INSTALL AND USE THE ESLINT AND PRETTIER !

### §VITE:

#### Vite é um build tool (ferramenta de construção) para aplicações web modernas

#### 1° npm create vite@latest my-react-app -- --template react

#### 2 ° cd folder deeper and follow the instructions of the terminal !!
============================================================
### (ESLINT E PRETTIER)

#### 1° npm init @eslint/config ( show the options to you configure)

#### 2° npm i --save-dev eslint-config-prettier

#### 3° npm install eslint-plugin-import-helpers eslint-import-resolver-typescript --save-dev ( organize the order of imports within the files.)

#### 4° create a folder .eslintignore and put in
#### /*.js
#### node_modules
#### dist

#### 5° npm install prettier eslint-config-prettier eslint-plugin-prettier --save-dev

#### 6° reference rules on .eslintrc.json
```json
{
"env": {
"browser": true,
"es2021": true,
"jest": true
},
"extends": [
"plugin:react/recommended",
"airbnb",
"plugin:@typescript-eslint/recommended",
"prettier",
"plugin:prettier/recommended"
],
"parser": "@typescript-eslint/parser",
"parserOptions": {
"ecmaFeatures": {
"jsx": true
},
"ecmaVersion": 12,
"sourceType": "module"
},
"plugins": [
"react",
"@typescript-eslint",
"eslint-plugin-import-helpers",
"prettier"
],
"rules": {
"camelcase": "off",
"import/no-unresolved": "error",
"@typescript-eslint/naming-convention": [
"error",
{
"selector": "interface",
"format": [
"PascalCase"
],
"custom": {
"regex": "^I[A-Z]",
"match": true
}
}
],
"class-methods-use-this": "off",
"import/prefer-default-export": "off",
"no-shadow": "off",
"no-console": "off",
"no-useless-constructor": "off",
"no-empty-function": "off",
"lines-between-class-members": "off",
"import/extensions": [
"error",
"ignorePackages",
{
"ts": "never",
"tsx": "never"
}
],
"import-helpers/order-imports": [
"warn",
{
"newlinesBetween": "always",
"groups": [
"module",
"/^@shared/",
[
"parent",
"sibling",
"index"
]
],
"alphabetize": {
"order": "asc",
"ignoreCase": true
}
}
],
"import/no-extraneous-dependencies": [
"error",
{
"devDependencies": [
"**/*.spec.js"
]
}
],
"prettier/prettier": "error",
"react/jsx-filename-extension": [
1,
{
"extensions": [
".jsx",
".tsx"
]
}
],
"react/react-in-jsx-scope": "off",
"no-use-before-define": "off",
"@typescript-eslint/no-use-before-define": [
"error"
]
},
"settings": {
"import/resolver": {
"typescript": {}
}
}
} 
```
=============================================================================
