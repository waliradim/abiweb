#editor setting as work

{
"explorer.confirmDelete": false,
"grunt.autoDetect": "on",
"git.autofetch": true,
"git.allowForcePush": true,
"git.enableSmartCommit": true,
"javascript.updateImportsOnFileMove.enabled": "always",
"editor.defaultFormatter": "esbenp.prettier-vscode",
"editor.formatOnPaste": true,
"editor.formatOnSave": true,
"editor.formatOnType": true,
"path-intellisense.autoSlashAfterDirectory": true,
"path-intellisense.autoTriggerNextSuggestion": true,
"path-intellisense.extensionOnImport": true,
"editor.fontSize": 16,

// config related to code formatting

"[javascript]": {
"editor.formatOnSave": false,
"editor.defaultFormatter": null
},
"[javascriptreact]": {
"editor.formatOnSave": false,
"editor.defaultFormatter": null
},
"javascript.validate.enable": false, //disable all built-in syntax checking
"editor.codeActionsOnSave": {
"source.fixAll.eslint": true,
"source.fixAll.tslint": true,
"source.organizeImports": true
},
"eslint.alwaysShowStatus": true,
// emmet
"emmet.triggerExpansionOnTab": true,
"emmet.includeLanguages": {
"javascript": "javascriptreact"
}
}

#On package.json
"lint": "npm add -D prettier && npm add -D babel-eslint && npx install-peerdeps --dev eslint-config-airbnb && npm add -D eslint-config-prettier eslint-plugin-prettier"

into script tag
and then open terminal and cmd npm run lint

#add new file on project root folder name .eslintrc and past the below code
{
"extends": [
"airbnb",
"airbnb/hooks",
"eslint:recommended",
"prettier",
"plugin:jsx-a11y/recommended"
],
"parser": "babel-eslint",
"parserOptions": {
"ecmaVersion": 8
},
"env": {
"browser": true,
"node": true,
"es6": true,
"jest": true
},
"rules": {
"react/react-in-jsx-scope": 0,
"react-hooks/rules-of-hooks": "error",
"no-console": 0,
"react/state-in-constructor": 0,
"indent": 0,
"linebreak-style": 0,
"react/prop-types": 0,
"jsx-a11y/click-events-have-key-events": 0,
"react/jsx-filename-extension": [
1,
{
"extensions": [".js", ".jsx"]
}
],
"prettier/prettier": [
"error",
{
"trailingComma": "es5",
"singleQuote": true,
"printWidth": 100,
"tabWidth": 4,
"semi": true,
"endOfLine": "auto"
}
]
},
"plugins": ["prettier", "react", "react-hooks"]
}
