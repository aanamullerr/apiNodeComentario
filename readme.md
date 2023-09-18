# Documentação da API

* Escolher um local do computador para criar o projeto
* Abrir o gitBash nesta pasta 

Com o gitBash aberto, executar o comando para criar a raiz do projeto: 

```
mkdir NOME_PROJETO
```

Acessar a pasta

```
cd NOME_PROJETO
```

Comando para abrir o VScode

```
code .
```

Criar o arquivo gerenciador de pacotes node

```
npm init -y
```

Criar arquivo .gitignore na raiz do projeto

```
touch .gitignore
```

Criar arquivo .env

```
touch .env
```

## Instalar os pacotes do projeto

```
npm i express nodemon dotenv
```

* express: será o servidor da api 
* nodemon: atualizar os arquivos alterados sem parar o servidor 
* dotevn: gerenciador de variáveis de ambiente

Criar pasta src

```
mkdir src
```

Criar arquivo server.js

```
touch src/server.js
```

Adicionar arquivos e pastas no .gitignore

```
node_modules
.env
```

Adicionar a porta do servidor no arquivo .env

```
PORT = 3000
```

Configuração básica da API com express

```
// Importar o pacote express
const express = require('express');

// Instanciar o express na variavel app
const app = express();

// Recuperar o pacote dotenv
const dotenv = require('dotenv').config();

// Importando variavel do arquivo .env
const PORT = process.env.PORT;

// Testando o servidor
app.listen(PORT, () => console.log(`Running at port ${PORT}!`))

```

Criar comando para rodar o servidor, no arquivo package.json

```
"start":"nodemon src/server.js"
```