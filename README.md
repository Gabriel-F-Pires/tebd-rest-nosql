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

