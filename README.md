# Diário-de-Classe: Exemplo prático de criação de uma API REST que utiliza um banco de dados NoSQL

Este repositório contém um exemplo simples de um sistema de Diário de Classe construído usando **o banco de dados NoSQL MongoDB**.

O objetivo da aula é permitir que o aluno tenha um primeiro contato com desenvolvimento de APIs que acessam uma base de dados NoSQL e com tecnologias normalmente usadas nesse tipo de arquitetura, tais como **Node.js**, **REST**, **MongoDB** e **Postman**.

## Executando o Sistema

A seguir vamos descrever a sequência de passos para você executar o sistema localmente em sua máquina. Ou seja, todo o sistema estará rodando na sua máquina.

**IMPORTANTE:** Você deve seguir esses passos antes de implementar as tarefas práticas descritas nas próximas seções.

1. Faça um fork do repositório. Para isso, basta clicar no botão **Fork** no canto superior direito desta página.

2. Vá para o terminal do seu sistema operacional e clone o projeto (lembre-se de incluir o seu usuário GitHub na URL antes de executar)

```
git clone https://github.com/<SEU USUÁRIO>/tebd-rest-nosql.git
```

3. É também necessário ter o **Node.js** instalado na sua máquina. Se você não tem, siga as instruções para instalação contidas nessa [página](https://nodejs.org/en/download/).

4. Por fim, é necessário ter o banco de dados **MongoDB** configurado. Se você não tem, siga as instruções para instalação contidas nessa [página](https://github.com/fabsfernandes/tebd-rest-nosql/blob/main/MONGODB-INSTALACAO.md)


5. Abra o arquivo `.env` e adicione a string de conexão correspondente ao seu cluster MongoDB. A string final irá parecer com algo como:

```
mongodb+srv://******:*****@cluster0.scd8qwp.mongodb.net/test
```

6. Em um terminal, vá para o diretório no qual o projeto foi clonado e instale as dependências necessárias para execução do sistema:

```
cd tebd-rest-nosql
npm install
```

7. Inicie o sistema através do comando:

```
npm run start
```

8.  Para fins de teste, efetue uma requisição para o sistema reponsável pela API do backend.

-   Se tiver o `curl` instalado na sua máquina, basta usar:

```
curl -i -X GET http://localhost:3000/api/hello
```

-   Caso contrário, você pode fazer uma requisição acessando, no seu navegador, a seguinte URL: `http://localhost:3000/api/hello`.


## Tarefa Prática #1: Testando a API

Nesta primeira tarefa, você irá testar as funcionalidade da API criada.

#### Passo 1

Primeiro, você deve instalar o software **Postman**, que será utilizado para chamadas às operações da API REST.
As instruções de instalação estão nesta [página](https://www.postman.com/downloads/)

#### Passo 2

Vamos agora fazer uma chamada para adicionar um aluno ao Diário de Classe.
Esta funcionalidade está exposta via API por meio de um serviço POST no seguinte endpoint:

```
localhost:3000/api/post
```

A operação exige que os dados sejam passados no formato JSON, no campo Body da chamada.
Crie um JSON contendo as informações de "name" e "age" conforme a imagem a seguir:

<p align="center">
    <img width="70%" src="https://github.com/fabsfernandes/tebd-rest-nosql/blob/main/Screen%20Shot%202022-11-22%20at%2000.27.27.png" />
</p>

Clique em `send`para fazer a requisição.

#### Passo 3

Observe o resultado. Ele deve ter o código 200 (OK).

#### Passo 4

Agora vamos fazer uma chamada para identificar todos os alunos que fazem parte do Diário de Classe.

Esta funcionalidade está exposta via API por meio de um serviço GET no seguinte endpoint:

```
localhost:3000/api/getAll
```

Nesta chamada, não é necessário enviar nenhum dado. É apenas uma chamada "GET".
Clique em `send`para fazer a requisição.

#### Passo 5

Observe o resultado. Ele deve ter o código 200 (OK), bem como todos os alunos do Diário de Classe.

## Tarefa Prática #2: Explorando demais funcionalidades da API

A API REST construída possui as seguintes operações:
POST
GET
DEL
PATCH

#### Passo 1

Realize uma chamada para cada operação.


## Tarefa Prática #3: Adicionando uma nova informação no Diário de Classe

Adicione o campo `nota` aos documentos do seu banco de dados.
