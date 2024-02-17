# spring-jwt-auth-api
 

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)


Este projeto é uma construção de API usando **Java, Spring, Postgres, Spring Security e JWT para controle de autenticação.**

## Conteúdo

- [Como funciona o JWT](#como-funciona-o-jwt)
- [Instalação](#instalação)
- [Iniciando o programa](#iniciando-o-programa)
- [API Endpoints](#api-endpoints)
- [Autenticação](#autenticação)
- [Database](#database)

## Como funciona o JWT

![1](https://github.com/VitorGabriel-TI/spring-jwt-auth-api/assets/128819057/69ae219d-2a88-4f3c-8dd4-00603b0b1fdd)

![2](https://github.com/VitorGabriel-TI/spring-jwt-auth-api/assets/128819057/b5f01200-837e-4f17-a896-18a29895a11d)

## Instalação

1. Clone o repositório:

```bash
git clone https://github.com/VitorGabriel-TI/spring-jwt-auth-api.git
```

2. Instale as dependências com o Maven

3. Instale [PostgresSQL](https://www.postgresql.org/)

## Iniciando o programa

1. Inicie a aplicação com o Maven
2. A API será acessível na porta http://localhost:8080


## API Endpoints
A API fornece os seguintes endpoints:

```markdown
GET /product - Busca uma lista de todos os produtos. (todos os usuários autenticados)

POST /product - Registrar um novo produto (necessário acesso ADMIN).

POST /auth/login - Login na aplicação

POST /auth/register - Registrar um novo usuário na aplicação
```

## Autenticação
A API usa Spring Security para o controle de autenticação. Usando as seguintes regras.

```
USUÁRIO -> Função de usuário padrão para usuários logados.
ADMIN -> Função administrativa para parceiros gestores (registo de novos parceiros).
```
Para acessar endpoints protegidos como usuário ADMIN, forneça as credenciais de autenticação apropriadas no cabeçalho da solicitação.

## Database
Este projeto utiliza [PostgresSQL](https://www.postgresql.org/) como banco de dados. As migrações de banco de dados necessárias são gerenciadas usando Flyway.


