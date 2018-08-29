# Lista de tarefas

Para rodar o projeto:
### `npm install`  
### `npm start`

Abra [http://localhost:3000](http://localhost:3000) no navegador.

A página atualiza automaticamente a cada alteração

## Projeto:

Uma lista de tarefas simples usando uma api REST.

- Lista de tarefas vindas da api
- Permitir adicionar uma nova tarefa
- Checkbox/Botão para completar a tarefa
- Botão para excluir a tarefa

_Obs_: Não é necessário terminar todas as funcionalidades, o layout da aplicação não é importante, o foco é demonstrar conhecimento de `React` e `REST`

# API

`url: https://api-ykcnvifmxi.now.sh`

_endpoints_:

## GET `/tarefa` - Lista todas as tarefas

Retorno

```
[
    {
        "id": "575a90e7-63ff-4aba-b221-50da4f3c9e0e",
        "titulo": "Comprar presente de aniversário",
        "concluido": false
    },
    {
        "id": "0c716e06-6046-4b8c-bd36-9f71b24a4642",
        "titulo": "Entregar o trabalho de Química",
        "concluido": false
    }
]
```

## POST `/tarefa` - Adiciona uma nova tarefa

Dados a serem enviados:

```
{
	"titulo": "Comprar pão",
	"concluido": false
}
```

Retorno:

```
{
    "titulo": "Comprar pão",
    "concluido": false,
    "id": "65997d30-eabb-4300-8b5f-25ad64951d1e"
}
```

## PUT `/tarefa/{id}` - Atualiza os dados da tarefa

ex: **PUT** `/tarefa/65997d30-eabb-4300-8b5f-25ad64951d1e`

Dados a serem enviados:

```
{
	"titulo": "Comprar leite",
	"concluido": true
}
```

Retorno com sucesso:

```
{
    "status": "ok"
}
```

Retorno com erro:

```
{
    "status": "erro",
    "mensagem": "id não encontrado"
}
```

## DELETE `/tarefa/id_da_tarefa` - remove uma tarefa

ex: **DELETE** `/tarefa/65997d30-eabb-4300-8b5f-25ad64951d1e`

Retorno com sucesso:

```
{
    "status": "ok"
}
```

Retorno com erro:

```
{
    "status": "erro",
    "mensagem": "registro não encontrado"
}
```

## GET `/reset` - reseta os dados para o estado inicial
