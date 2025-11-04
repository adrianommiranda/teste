📚 API de Gerenciamento de Usuários
Esta aplicação é uma API REST desenvolvida com Spring Boot para gerenciar o cadastro de usuários, permitindo operações de cadastro, consulta, atualização e exclusão (CRUD).

🚀 Como funciona
A API expõe endpoints RESTful para manipulação de usuários. Os dados são persistidos em um banco de dados relacional utilizando o Spring Data JPA, e o mapeamento entre entidades (Usuario) e objetos de transferência de dados (UsuarioDTO) é feito com a biblioteca ModelMapper.

✨ Principais funcionalidades
Listar todos os usuários
GET
/usuario/listartodos
Buscar usuário por ID
GET
/usuario/id/{id}
Buscar por nome exato
GET
/usuario/nome/{nome}
Buscar por nome (ignorando maiúsculas/minúsculas)
GET
/usuario/nomeignore/{nome}
Buscar por nome contendo (case-insensitive)
GET
/usuario/nomeignorecontaining/{nome}
Criar novo usuário
POST
/usuario/salvar
Atualizar usuário
PUT
/usuario/atualizar/{id}
Remover usuário
DELETE
/usuario/delete/{id}

💡 Consulte os exemplos de uso no Postman ou outro cliente HTTP. 

⚙️ Como executar
Pré-requisitos
Java 17+
Maven
MySQL 8.0+
Configuração do banco de dados
Crie um banco de dados chamado usuario com as seguintes credenciais:

Usuário: root
Senha: 31211
🔒 Atenção: Essas credenciais são para ambiente de desenvolvimento. Em produção, use variáveis de ambiente ou configurações seguras. 

Os arquivos de configuração estão localizados em:



1
2
3
src/main/resources/application.properties
src/main/resources/application-dev.properties
src/main/resources/application-test.properties
Inicialização
Clone ou baixe o projeto.
Navegue até o diretório raiz.
Execute o comando:
bash


1
mvn spring-boot:run
A API estará disponível em: http://localhost:8080

🌐 Perfis do Spring Boot
default
Execução normal da aplicação.
dev
Ambiente de desenvolvimento (banco local).
test
Inicializa o banco com dados de teste automaticamente.

Para ativar um perfil específico:

bash


1
mvn spring-boot:run -Dspring-boot.run.profiles=test
📦 Dependências principais
Spring Boot (v3.5+)
Spring Data JPA
ModelMapper
MySQL Connector
Spring Web
Jakarta Validation
📚 Documentação adicional
Spring Boot Reference Guide
Spring Data JPA Documentation
ModelMapper
✨ Desenvolvido com ❤️ por [Seu Nome]
Para dúvidas ou sugestões, abra uma issue ! 