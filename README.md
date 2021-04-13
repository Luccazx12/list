# List React
Aplicação contendo **ReactJS** + **Bootstrap** baseado no tutorial do WebSite [Celke](https://celke.com.br/artigo/como-integrar-o-react-com-bootstrap).

**Hospeadado em: [Netlify](https://list-reactjs.netlify.app/)**


&nbsp;


# Requisitos


## **Ambientes de Desenvolvimento e Referências**

* IDE:    **VSCODE 1.55.1**
* [Node.js](https://nodejs.org/en/):    **version 14.16.0 (x64) and NPM**

## Instalações

**Yarn** - Através do NPM iremos instalar o gerenciador de dependências do Facebook Yarn, que é mais recomendado para se trabalhar usando o React:

```
npm install -g yarn
````

**Create-react-app** - Precisamos instalar a ferramenta de Linha de comando create-react-app que também foi desenvolvida pelo Facebook para criarmos um projeto do zero sem nos preocuparmos com bundling, otimização de arquivo e outros detalhes de configuração que podem ser extensos quando realizados manualmente:

```
npm install -g create-react-app
````


&nbsp;


# Primeiros passos para criar sua aplicação React

1 - Dentro da pasta do seu projeto, execute o seguinte comando: 
```sh
create-react-app aplicacao
```

2 - Esse comando criará vários arquivos dentro da pasta *aplicacao*, dentre eles, pacotes. Para continuarmos a instalação desses pacotes, digite o seguinte comando para acessarmos a pasta do nosso projeto:
```
cd aplicacao
````

3 - Logo após, ainda no mesmo diretório, para instalação dos pacotes do Bootstrap, execute os seguintes comandos:
```
npm install --save react react-dom
npm install --save react-bootstrap
````

4 - Para começar a programar, vamos utilizar a IDE Visual Studio Code. Para abrir o projeto nele, digite os seguintes comandos no diretório do projeto:
```
code .
````

5 - Pronto! Agora basta você desenvolver do seu jeito a sua aplicação e executa-lá para teste com o comando a seguir:
```
yarn start
````
