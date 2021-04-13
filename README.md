# List React

Lista de compras desenvolvida em ReactJS com utilização do Hooks useState.

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
npx create-react-app list
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

&nbsp;


## Hooks - UseState

UseState é uma nova forma de definir e atualizar (mutar) o estado “interno ”de um componente. Mais limpo e menos verboso esse é com certeza um dos melhores hooks lançados nessa versão 16.8.

1 - Vamos importar ele da seguinte forma no App.js: 
```
import React, { useState } from 'react';
````

2 - Logo em seguida, o utilizaremos no App.js:
```
const [item, setItem] = useState('');
````

3 - E como nosso código depende de um INPUT, precisamos modifica-lo da seguinte forma para funcionar com o useState:
```
<input type="text" placeholder="Item" value={item} name="item" onChange = {e => setItem(e.target.value)} />
````

4 -  Além disso, precisamos de duas coisas:

- Um outro estado capaz de armazenar uma lista
- Uma função que seja capaz de adicionar o valor à lista

*Para criarmos outro estado, é simples:*
```
const [itemList, setItemList] = useState([])
````

*E a função para conseguirmos adicionar itens também:*
```
const addItem = () => {
    setItemList([item].concat(itemList))
    setItem('')
}
````

5 - Também precisamos garantir que a função addItem que criamos seja chamada quando clicarmos no botão para inserir o que foi escrito no input dentro da lista. Para isso, vamos inserir um evento Onclick, referenciando o addItem:
```
<button onClick={addItem}>Adicionar Item</button>
````

6 - Para finalizar, temos que dar uma estrutura de lista para nosso código, e que essa estrutura receba os itens dentro do Array (array vazio do segundo estado que criamos) e renderize na tela. Para isso vamos utilizar o map:
```
      <ul>
        {itemList.map((item) => (
          <li>{item}</li>
        ))}
      </ul>
````
