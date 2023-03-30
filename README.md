# CONFIGURAÇÕES INICIAIS PARA UM PROJETO REACT COM JS, EDITORCONFIG, PRETTIER, ESLINT E PROP-TYPES

- comando para criar um projeto react na pasta local:
`npx create-react-app .`

- instalar a extensão para o VSCode "EditorConfig for VS Code"
clicar com botão direito na árvore de diretórios do projeto e então em "Generate .editorconfig"

- No arquivo criado .editorconfig, colocar as seguintes linhas:
```
	# EditorConfig is awesome: https://EditorConfig.org
	# top-most EditorConfig file
	root = true
	[*]
	indent_style = space
	indent_size = 2
	end_of_line = lf
	charset = utf-8
	trim_trailing_whitespace = true
	insert_final_newline = true
```

- criar os seguintes arquivos na raiz do projeto, com seus respectivos conteúdos de configuração:

`.eslintrc.js`

```
	module.exports = {
	  env: {
	    browser: true,
	    es2021: true,
	    jest: true,
	  },
	  extends: [
	    'eslint:recommended',
	    'plugin:react/recommended',
	    'plugin:react-hooks/recommended',
	    'plugin:prettier/recommended',
	  ],
	  parserOptions: {
	    ecmaFeatures: {
	      jsx: true,
	    },
	    ecmaVersion: 12,
	    sourceType: 'module',
	  },
	  plugins: ['react'],
	  settings: {
	    react: {
	      version: 'detect',
	    },
	  },
	  rules: {
	    'react/react-in-jsx-scope': 'off',
	  },
	};
```

`.prettierrc.js`

```
	module.exports = {
	  semi: true,
	  trailingComma: 'all',
	  singleQuote: true,
	  printWidth: 120,
	  tabWidth: 2
	}
```

- Depois rodar os seguinte comando no terminal para que as configurações sejam carregadas adequadamente

`npm i -D prettier eslint-config-prettier eslint-plugin-prettier`

- Pronto! O Prettier e o ESlint estão configurados. Para que eles corrijam todos os arquivos de seu projeto (tanto os .js quanto os .jsx) rode os seguintes comandos:

`npx eslint src/**/*.js --fix`
`npx eslint src/**/*.jsx --fix`

- Vale a pena já instalar o Prop-Types, para já deixar tudo pronto:

`npm i prop-types`

_______________
# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).
## Available Scripts
In the project directory, you can run:
### `npm start`
Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.
The page will reload when you make changes.\
You may also see any lint errors in the console.
### `npm test`
Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.
### `npm run build`
Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.
The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!
See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.
### `npm run eject`
**Note: this is a one-way operation. Once you `eject`, you can't go back!**
If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.
Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.
You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.
## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).
To learn React, check out the [React documentation](https://reactjs.org/).
### Code Splitting
This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)
### Analyzing the Bundle Size
This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)
### Making a Progressive Web App
This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)
### Advanced Configuration
This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)
