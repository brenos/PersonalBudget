# Personal Budget Project

## Descrição

Projeto backend de Orçamento Pessoal simples para estudos ou inicio do desenvolvimento de um produto. Foi realizado com o intuito de aperfeiçoamento e paixão pela linguagem usada.

## Funcionalidades
**Categorias**

| Method | Path                       | Descrição                        |
| ------ | -------------------------- | -------------------------------- |
| GET    | ../categorie/{userId}      | Retorna as categorias do usuário |
| POST   | ../categorie               | Insere uma categoria do usuário  |
| PUT    | ../categorie/{categorieId} | Altera a categoria do usuário    |
| DELETE | ../categorie/{categorieId} | Exclui a categoria do usuário    |

____

**Tipo de Transação**

| Method | Path                                   | Descrição                                       |
| ------ | -------------------------------------- | ----------------------------------------------- |
| GET    | ../transactiontype                     | Retorna todos os tipos de transações existentes |
| GET    | ../transactiontype/{transactionTypeId} | Retorna o tipo de transação pelo seu id         |
| POST   | ../transactiontype                     | Insere um tipo de transação                     |
| PUT    | ../transactiontype/{transactionTypeId} | Altera um tipo de transação                     |
| DELETE | ../transactiontype/{transactionTypeId} | Exclui um tipo de transação                     |

____

**Transação**

| Method | Path                           | Descrição                                      |
| ------ | ------------------------------ | ---------------------------------------------- |
| GET    | ../transaction/{userId}        | Retorna o tipo de transação pelo id do usuário |
| POST   | ../transaction                 | Insere uma transação                           |
| PUT    | ../transaction/{transactionId} | Altera uma transação                           |
| DELETE | ../transaction/{transactionId} | Exclui uma transação                           |

____

**Lançamento**

| Method | Path                       | Descrição                               |
| ------ | -------------------------- | --------------------------------------- |
| GET    | ../release/{transactionId} | Retorna os lançamentos de uma transação |
| POST   | ../release                 | Insere um lançamento                    |
| PUT    | ../release/{releaseId}     | Altera um lançamento                    |
| DELETE | ../release/{releaseId}     | Exclui um lançamento                    |

## Informações Técnicas

Api versionada conectando ao Banco de Dados (Desenvolvido com o MySQL), podendo usar uma conexão de réplica para as consultas.
<br/>
Na pasta <b>MySQL Model</b> contém o DER da base de dados.
<br/>
Na pasta <b>PostmanCollection</b> contém uma coleção do postman com todos os endpoints.

## Como instalar

#### Mac / Linux
dotnet build
<br/>
dotnet ef database update

Obs.: Alterar context, adicionar ou remover colunas ou tabelas
- dotnet ef migrations add AddColumnTable

#### Windows (Command line)
update-database

Obs.: Alterar context, adicionar ou remover colunas ou tabelas
- add-migration AddColumnTable

## Stack utilizada
- .Net Core 3.1
- Entity Framework
- ApiVersioning
- NUnit


## Referencias
https://docs.microsoft.com/en-us/dotnet/core/introduction
<br/>
https://docs.microsoft.com/en-us/ef/core/managing-schemas/migrations/?tabs=dotnet-core-cli
<br/>
https://docs.microsoft.com/en-us/dotnet/core/testing/unit-testing-with-nunit
