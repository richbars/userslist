# Documentação Técnica - API de Usuários

## Objetivo

A API tem como objetivo permitir a inserção, atualização, exclusão e consulta de informações de usuários em um banco de dados MySQL.

## Informações dos Usuários

A API manipula as seguintes informações para cada usuário:

1. **Nome**: Nome completo do usuário.
2. **CPF**: Número do CPF do usuário.
3. **Endereço (CEP)**: Código de Endereço Postal (CEP) do usuário.
4. **Telefone**: Número de telefone (pode ser celular ou fixo).

## O que é uma API?

API (Interface de Programação de Aplicações) é um conjunto de regras que permite que diferentes aplicações se comuniquem entre si. Elas definem como os sistemas interagem, permitindo a troca de dados de forma estruturada e padronizada.

## Funcionalidades da API

A API oferece as seguintes funções para manipulação dos dados dos usuários:

1. **Insert (Inserir)**  
   A função `Insert` permite inserir as informações de um novo usuário na base de dados. Ao enviar os dados via API, o usuário será adicionado ao banco de dados MySQL.

   **Método HTTP**: `POST`  
   **Endpoint**: `/usuarios`  
   **Exemplo de dados**:
   ```json
   {
     "nome": "João Silva",
     "cpf": "123.456.789-00",
     "cep": "12345-678",
     "telefone": "(11) 91234-5678"
   }


2. **Delete (Deletar)**
A função `Delete` permite remover um usuário da base de dados, utilizando o ID do usuário como parâmetro para identificar o registro a ser excluído.

- **Método HTTP**: `DELETE`
- **Endpoint**: `/usuarios/{id}`
- **Exemplo de requisição**:  
  `DELETE /usuarios/1`

- **Descrição**: Ao enviar a requisição para o endpoint com o ID do usuário, a API remove o usuário correspondente da base de dados.

3. **Update (Atualizar)**
A função `Update` permite atualizar as informações de um usuário existente na base de dados, utilizando o ID para identificar o usuário a ser modificado.

- **Método HTTP**: `PUT`
- **Endpoint**: `/usuarios/{id}`
- **Exemplo de dados**:
  ```json
  {
    "nome": "João Silva",
    "cpf": "123.456.789-00",
    "cep": "12345-678",
    "telefone": "(11) 98765-4321"
  }
