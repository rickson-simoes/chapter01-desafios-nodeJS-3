<h1>Aplicação já existente, porém, com erros para serem corrigidos.</h1>

[![Package][nodemon-image]][nodemon-url] 
[![Technology][node-image]][node-url] 


[nodemon-url]: https://www.npmjs.com/package/nodemon
[nodemon-image]: https://img.shields.io/badge/Nodemon-green?style=for-the-badge&logo=Nodemon&logoColor=black

[node-url]: https://nodejs.org/
[node-image]: https://img.shields.io/badge/NodeJS-green?style=for-the-badge&logo=Node-dot-js&logoColor=black

---
## Instruções para uso:

1º - yarn install

2º - yarn dev

3º - yarn test (Para verificar se todas as tarefas foram executadas.)

---

- *Essa aplicação realiza o CRUD (Create, Read, Update, Delete) de repositórios de projetos.* 
- *Além disso, é possível dar likes em repositórios cadastrados, aumentando a quantidade de likes em 1 a cada vez que a rota é chamada.*

---

Descrição de cada propriedade:
- **id** deve ser um uuid válido;
- **title** é o título do repositório (por exemplo "unform");
- **url** é a URL que aponta para o repositório (por exemplo "[https://github.com/unform/unform](https://github.com/unform/unform)");
- **techs** é um array onde cada elemento deve ser uma string com o nome de uma tecnologia relacionada ao repositório (por exemplo: ["react", "react-native", "form"]);
- **likes** é a quantidade de likes que o repositório recebeu (e que vai ser incrementada de 1 em 1 a cada chamada na rota de likes).

**A quantidade de likes deve sempre ser zero no momento da criação.**

---

## Rotas
 
### GET `/repositories`
A rota deve retornar uma lista contendo todos os repositórios cadastrados.

### POST `/repositories`
A rota deve receber `title`, `url` e `techs` pelo corpo da requisição e retornar um objeto com as informações do repositório criado e um status `201`.

### PUT `/repositories/:id`
A rota deve receber `title`, `url` e `techs` pelo corpo da requisição e o `id` do repositório que deve ser atualizado pelo parâmetro da rota. Deve alterar apenas as informações recebidas pelo corpo da requisição e retornar esse repositório atualizado.

### DELETE `/repositories/:id`
A rota deve receber, pelo parâmetro da rota, o `id` do repositório que deve ser excluído e retornar um status `204` após a exclusão.

### POST `/repositories/:id/like`
A rota deve receber, pelo parâmetro da rota, o `id` do repositório que deve receber o like e retornar o repositório com a quantidade de likes atualizada.