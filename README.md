# Deploy VueJS
Fazendo deploy de um app default do VueJS no GitHub Pages<br/>
<Strong>VueJS: </Strong>(https://vuejs.org/)<br/>
<Strong>gh-pages: </Strong>(https://www.npmjs.com/package/gh-pages)<br/>
<Strong>Demo: </Strong>(https://ewertonbello.github.io/deploy-vuejs/)

### Procedimento

1. Crie um repositório e vincule seu projeto a ele, na pasta do seu projeto faça:
    ```
    git init
    git add .
    git commit -m "primeiro commit"
    git remote add origin https://github.com/NomeDeUsuario/nome-do-repositorio.git
    git push -u origin master
    ```
2. Depois crie na raiz do projeto um arquivo chamado `vue.config.js`, dentro desse arquivo insira `module.exports = { publicPath: '/nome-do-repositorio'}`. 
<br/>Exemplo:
    ```
    module.exports = {
	  publicPath: '/deploy-vuejs'//Nome do repositório
    }
    ```
3. Agora faça o build do seu app, dentro da pasta do seu projeto execute `npm run build` ou `yarn build` se preferir utilizar o yarn.
4. Depois utilize o comando `npx gh-pages -d dist` para fazer o deploy da pasta dist do seu app no branch gh-pages, utilizando o pacote gh-pages.
