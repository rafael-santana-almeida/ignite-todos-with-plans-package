<h1 align="center">Todos com plano - Ignite | Rocketseat :rocket:</h1> 

## :memo: Descrição e funcionalidades

Essa é uma pequena API desenvolvida em **NodeJS**, como segundo desafio do bootcamp Ignite da Rocketseat, onde consiste em uma aplicação de gerenciamento de Tarefas (*todos*). Nessa segunda versão, foi adicionado a modalidade de plano gratuito, onde poderá ser adicionado até 10 tarefas por usuário, e o plano PRO, que não possui limite de tarefas.

A API roda em http://localhost:3333 e possuí as seguintes rotas/funcionalidades:

* `POST /users :` Rota para criação de um novo usuário. Deve ser informado as informações de `name` e `username` no corpo da requisição. 
``` 
{
  "name": "Fulando de tal da silva",
  "username": "Nome de usuário"
}
```

* `GET /users/:id :` Rota para consulta de usuário com base no `id` informado na rota. 

* `PATCH /users/:id/pro :` Rota para liberar o plano PRO pra o usuário. Deve ser informado o `id` do usuário na rota. 

* `GET /todos :` Rota para captura de todas as tarefas (*todos*) de um usuário. No Header da requisição deve ser informado o `username` do usuário.   

* `POST /todos :` Rota para criação de uma nova tarefa (*todo*). No Header da requisição deve ser informado o `username` do usuário, e no corpo, as informações de `title` e `deadline`.
```
{
  "title": "Titulo da tarefa",
  "deadline": "Data no formtato yyyy-mm-dd"
}
```

* `PUT /todos/:id :` Rota para a alteração das informações de uma tarefa (*todo*). No Header da requisição deve ser informado o `username` do usuário, e no corpo, as informações de `title` e `deadline`.
```
{
  "title": "Titulo alterado",
  "deadline": "Data alterada no formato yyyy-mm-dd"
}
```

* `PATCH /todos/:id/done :` Rota para concluir uma tarefa (*todo*). No Header da requisição deve ser informado o `username` do usuário.

* `DELETE /todos/:id :` Rota para excluir uma tarefa (*todo*). No Header da requisição deve ser informado o `username` do usuário.

## :wrench: Instalação
Para rodar essa aplicação, será necessário possuir o  `Node` instalado na máquina, e um gerenciador de pacotes (nesse projeto estou utilizando o `yarn`).

Após o repositório ter sido clonado, execute o comando `yarn` para instalar das dependencias. (`express`, `nodemon`, `cors`, `uuid`, `jest` e `supertest`)

Com as dependências instaladas, execute o comando abaixo para inicializar o servidor:

```
yarn dev
```
