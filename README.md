# Code challenge PUMA

## Instruções básicas

Você foi encarregado de construir um aplicativo web para a criação de uma lista
de usuários favoritos do GitHub.

Para isso, deverá ser utilizada a API oficial do GitHub (https://api.github.com)
cuja documentação se encontra em https://docs.github.com/pt/rest

A aplicação consistirá em um backend, que será responsável pelas requisições à
API do GitHub e persistência dos dados em memória.

A linguagem de programação deverá ser Javascript. Utilize Node.js e um
framework como Express.js ou Fastify para o backend, e React, Angular ou Vue.js
para o frontend.

## Backend

O backend de sua aplicação consistirá nas seguintes rotas:

```
GET /repos: listagem dos repositórios favoritos salvos em memória

POST /repos: adicionar um repositório à lista de favoritos

DELETE /repos/{username}: remover um repositório da lista de favoritos

PATCH /repos/{username}/star: marca um repositório da lista de favoritos com uma estrela

```

Regras de negócio:

- O usuário poderá adicionar o máximo de 5 repositórios favoritos;
- Somente 1 repositório pode ser marcado com uma estrela. Se o usuário tentar
  marcar um segundo repositório com uma estrela, o repositório anteriormente marcado
  deixará de ter a estrela;
- O usuário poderá ordenar a lista de repositórios em ordem alfabética de nome.

## Frontend

A aplicação web consistirá de uma entrada de texto onde o utilizador deverá
digitar o username do GitHub que deseja adicionar à lista de favoritos.

Ao clicar no botão adicionar, o usuário do GitHub escolhido deverá ser
adicionado à lista, que consistirá de cards contendo foto, nome do usuário e
username.

Para cada usuário adicionado deverá existir um botão de excluir, e outro botão
de estrela.

Acrescentar um botão para ordenar a lista em ordem alfabética de nome.

## Observações

- Caso o usuário tente inserir um username que não existe no GitHub, uma
  mensagem de erro deve ser exibida;
- Exibir mensagem de erro caso o usuário tente adicionar um novo username quando
  o limite de favoritos tiver sido alcançado;
- Não é necessário salvar a lista de favoritos em banco dados, podendo ficar
  somente em memória;
- Utilizar testes unitários no backend;
- Utilizar os princípios de programação orientada a objetos, design patterns e
  arquitetura limpa quando apropriado.
- Crie um arquivo README.md contendo uma explicação resumida de como implementou
  sua aplicação, quais frameworks utilizou, bem como instruções de como executar
  sua aplicação.

Boa sorte!
