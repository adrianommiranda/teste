# API de Gerenciamento de Usuários

Esta aplicação é uma API REST desenvolvida com Spring Boot para gerenciar o cadastro de usuários, permitindo operações de cadastro, consulta, atualização e exclusão (CRUD).

## Como funciona

A API expõe endpoints RESTful para manipulação de usuários. Os dados são persistidos em um banco de dados relacional utilizando o Spring Data JPA, e o mapeamento entre entidades (Usuario) e objetos de transferência de dados (UsuarioDTO) é feito com a biblioteca ModelMapper.

### Principais funcionalidades
- **Contexto de aplicação: **/crud-usuario

- **Listar todos os usuários:** `GET /usuario`
- **http://localhost:8080/crud-usuario/usuario

- **Buscar por nome exato:** `GET /usuario/nome/{nome}`
- **http://localhost:8080/crud-usuario/usuario/nome/Adriano

- **Buscar usuário por ID:** `GET /usuario/id/{id}`
- **http://localhost:8080/crud-usuario/usuario/id/10

- **Buscar por nome contendo (case-insensitive):** `GET /usuario/nomeignorecontaining/{nome}`
- **http://localhost:8080/crud-usuario/usuario/nomeignorecontaining/Marian

- **Buscar por nome (ignorando maiúsculas/minúsculas):** `GET /usuario/nomeignore/{nome}`
- **http://localhost:8080/crud-usuario/usuario/nomeignore/adr

- **Lista de nomes contendo (ignorando maiúsculas e minúsculas):** `GET /usuario/nome/containing/{nome}`
- **http://localhost:8080/crud-usuario/usuario/nome/containing/CA

- **Lista de usuarios com idade > idade de entrada:** `GET /usuario/idade/maior-que/{idade}`
- **http://localhost:8080/crud-usuario/usuario/idade/maior-que/18

- **Lista de usuarios com idade < idade de entrada:** `GET /usuario/idade/menor-que/{idade}`
- **http://localhost:8080/crud-usuario/usuario/idade/menor-que/18

- **Lista de usuarios com idade entre idade min e idade max:** `GET /usuario/idade/entre/{min}/{max}`
- **http://localhost:8080/crud-usuario/usuario/idade/entre/8/10

- **Contagem total de usuários:** `GET /usuario/total`
- **http://localhost:8080/crud-usuario/usuario/total

- **Contagem de usuários com idade maior que o valor informado** `GET /usuario/idade/maior-que/{idade}/total`
- **http://localhost:8080/crud-usuario/usuario/idade/maior-que/50/total

- **Lista de usuários com idade fora do intervalo 20 a 30** `GET /usuario/idade/entre2030`
- **http://localhost:8080/crud-usuario/usuario/idade/entre2030

- **Lista de usuários com idade fora do intervalo x a y** `GET /usuario/idade/fora-do-intervalo/{min}/{max}`
- **http://localhost:8080/crud-usuario/usuario/idade/fora-do-intervalo/20/30

- **Média de idade dos usuários** `GET /usuario/relatorios/media-idade`
- **http://localhost:8080/crud-usuario/usuario/relatorios/media-idade



- **Criar novo usuário:** `POST /usuario`
- **http://localhost:8080/crud-usuario/usuario

- **Atualizar usuário:** `PUT /usuario/{id}`
- **http://localhost:8080/crud-usuario/usuario/100

- **Remover usuário:** `DELETE /usuario/{id}`
- **http://localhost:8080/crud-usuario/usuario/100



### Pré-requisitos

1. Certifique-se de ter o Java 17+ instalado.
2. Maven instalado.
3. MySQL 8.0+

### Configuração do banco de dados

1. Crie um banco de dados chamado usuario com as seguintes credenciais: Usuário: root	Senha: 31211

### Os arquivos de configuração estão localizados em:

   ```sh
   src/main/resources/application.properties
   src/main/resources/application-dev.properties
   src/main/resources/application-test.properties
   ```

### Inicialização

1. Clone ou baixe o projeto.
2. Navegue até o diretório raiz.
3. Execute o comando:

   ```sh
   mvn spring-boot:run
   ```

4. A API estará disponível em: http://localhost:8080


### Como executar

1. Certifique-se de ter o Java 17+ e o Maven instalados.
2. Configure o banco de dados em `src/main/resources/application.properties`.
3. Execute o comando:

   ```sh
   mvn spring-boot:run
   ```

4. Acesse os endpoints via Postman, Insomnia ou qualquer cliente HTTP.

### Perfis

- **default:** Execução normal da aplicação.
- **dev:** Ambiente de desenvolvimento (banco local).
- **test:** Inicializa o banco com dados de teste automaticamente.

### Dependências principais

- Spring Boot (v3.5+)
- Spring Data JPA
- ModelMapper
- MySQL Connector
- Spring Web
- Jakarta Validation

### Documentação adicional

* [Spring Boot Reference](https://docs.spring.io/spring-boot/3.5.3/reference/htmlsingle/)
* [Spring Data JPA](https://spring.io/projects/spring-data-jpa)
* [ModelMapper](https://modelmapper.org/?spm=a2ty_o01.29997173.0.0.3774c921duLDBX)

---
 *  Desenvolvido por [Adriano]