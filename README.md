<div align="center"><img src="https://i.imgur.com/gYf4WfG.png" alt="Logo do Projeto" width="150" /><h1>🚀 Workshop Spring Boot 3 & JPA </h1><p><strong>Um projeto de workshop que constrói uma API RESTful com Spring Boot 3, Spring Data JPA e um banco de dados H2 in-memory.</strong></p><p><img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot"><img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java"><img src="https://img.shields.io/badge/Gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white" alt="Gradle"><img src="https://img.shields.io/badge/H2%20Database-FF0000?style=for-the-badge&logo=h2&logoColor=white" alt="H2 Database"><details><summary><strong>📚 Tabela de Conteúdos</strong></summary><ol><li><a href="#-sobre-o-projeto">📖 Sobre o Projeto</a></li><li><a href="#-funcionalidades-principais">✨ Funcionalidades Principais</a></li><li><a href="#-pilha-de-tecnologias-tech-stack">🛠️ Pilha de Tecnologias (Tech Stack)</a></li><li><a href="#-destaques-da-arquitetura">🔑 Destaques da Arquitetura</a></li><li><a href="#-começando-getting-started">🚀 Começando (Getting Started)</a></li><li><a href="#-endpoints-da-api">🛰️ Endpoints da API</a></li><li><a href="#-estrutura-de-ficheiros">📂 Estrutura de Ficheiros</a></li><li><a href="#-como-contribuir">🤝 Como Contribuir</a></li><li><a href="#-autor">👨‍💻 Autor</a></li><li><a href="#-licença">📄 Licença</a></li></ol></details>

-----------------------------------------------------------------------------------------------------------------------------
📖 Sobre o Projeto

  Este projeto é um workshop prático focado em construir uma API RESTful moderna usando Spring Boot 3. O objetivo principal é demonstrar a configuração de um projeto Java do zero, cobrindo os conceitos essenciais de Spring Data JPA para mapeamento objeto-relacional (ORM) e Spring Web para a criação de endpoints web.
  
  A aplicação expõe uma API simples para gerir "Utilizadores", utilizando um banco de dados H2 in-memory para facilitar os testes e o desenvolvimento sem a necessidade de configuração de um banco de dados externo.
  
-----------------------------------------------------------------------------------------------------------------------------
✨ Funcionalidades Principais

  1. 🌐 API RESTful: Expõe endpoints HTTP (como GET /users) para operações de CRUD (neste demo, apenas Read).
  
  2. 🗃️ Mapeamento JPA: Utiliza Spring Data JPA para mapear a classe User a uma tabela de banco de dados (tb_user).
  
  3. ⚡ Banco de Dados H2: Configurado para rodar em memória, permitindo que a aplicação seja executada instantaneamente.
  
  4. 🖥️ Console H2: O console web do H2 é ativado para fácil visualização e depuração do banco de dados em http://localhost:8080/h2-console.
  
  5. 🛠️ Build com Gradle: O projeto é gerido e compilado usando o Gradle.
    
-----------------------------------------------------------------------------------------------------------------------------
🛠️ Pilha de Tecnologias (Tech Stack)

  As principais tecnologias e dependências usadas neste projeto são:
  
  1. Framework (Spring Boot 3): Framework principal da aplicação.
  
  2. Linguagem (Java 17+): Linguagem de programação.
  
  3. API Web (Spring Web): Criação de controllers e endpoints REST.
  
  4. Base de Dados (ORM): Spring Data JPA. Mapeamento Objeto-Relacional.
  
  5. Base de Dados (Runtime): H2 Database. Banco de dados leve e em memória.
  
  6. Build Tool (Gradle): Gestor de dependências e build.
  
  7. Testes (Spring Boot Test): Framework de testes unitários e de integração.

-----------------------------------------------------------------------------------------------------------------------------
🔑 Destaques da Arquitetura

  O projeto é dividido em camadas clássicas do Spring Boot:
  
  1. Entidade (User.java)A classe de modelo que representa os dados. É anotada com @Entity para que o JPA saiba como mapeá-la para o banco de dados.
  
  2. Resource / Controller (UserResource.java)A classe que expõe a lógica de negócio para o mundo exterior através de endpoints REST.

  3. Configuração (application.properties): Onde a aplicação é configurada, incluindo a conexão com o H2 e a ativação do console. (Properties# Em src/main/resources/application.properties)

    # Configuração do H2 Database (em memória)
    spring.datasource.url=jdbc:h2:mem:testdb
    spring.datasource.username=sa
    spring.datasource.password=

    # Ativa o console do H2
    spring.h2.console.enabled=true

-----------------------------------------------------------------------------------------------------------------------------
🚀 Começando (Getting Started)

  Para executar este projeto localmente, siga estes passos.
  
  1. Pré-requisitosJava (JDK) 17 ou superior.
  
  2. Gradle (O gradlew wrapper está incluído no projeto e fará o download automático).
  
  3. Uma IDE Java (como IntelliJ IDEA ou VS Code com extensões Java).
  
  4. Guia de Instalação

     Clone o repositório:

         git clone https://github.com/victorhjsantiago/workshop-springboot3-jpa.git
         cd workshop-springboot3-jpa

      Execute a Aplicação:Use o wrapper do Gradle para compilar e iniciar o servidor Spring Boot.

       # No Linux / macOS
      ./gradlew bootRun

      # No Windows
      .\gradlew.bat bootRun

      Aceda aos Endpoints:A aplicação estará a ser executada em http://localhost:8080.

      API de Utilizadores: http://localhost:8080/users

      Console H2: http://localhost:8080/h2-consoleJDBC

      URL: jdbc:h2:mem:testdbUsername: saPassword: (deixe em branco)

----------------------------------------------------------------------------------------------------------------------------
📂 Estrutura de Ficheiros

workshop-springboot3-jpa/

├── build.gradle                # <--- Dependências e build do Gradle

├── gradle/

│   └── wrapper/                # Wrapper do Gradle

├── gradlew

├── gradlew.bat

├── src/

│   ├── main/

│   │   ├── java/com/course/course/

│   │   │   ├── CourseApplication.java  # <--- Ponto de entrada (main)

│   │   │   ├── entities/

│   │   │   │   └── User.java       # <--- Entidade JPA

│   │   │   └── resources/

│   │   │       └── UserResource.java # <--- Controller REST

│   │   └── resources/

│   │       └── application.properties # <--- Configuração da BD H2

│   └── test/

│       └── java/com/course/course/

│           └── CourseApplicationTests.java # Testes de integração

└── README.md

----------------------------------------------------------------------------------------------------------------------------
🤝 Como Contribuir

  Contribuições são o que tornam a comunidade open-source um lugar incrível para aprender, inspirar e criar. Qualquer contribuição que fizer será imensamente apreciada. 
  
  Se tiver uma sugestão para melhorar este projeto (mesmo sendo um demo!), por favor, faça um fork do repositório e crie um pull request.
  
  1. Faça um Fork do Projeto
  
  2. Crie a sua Feature Branch (git checkout -b feature/NovaFeatureIncrivel)
  
  3. Faça Commit das suas mudanças (git commit -m 'Adiciona NovaFeatureIncrivel')
  
  4. Faça Push para a Branch (git push origin feature/NovaFeatureIncrivel)
  
  5. Abra um Pull Request

  Não se esqueça de dar uma estrela ⭐️ ao projeto!
  
-----------------------------------------------------------------------------------------------------------------------------  
  👨‍💻 Autor
  <div align="center"><strong>Victor H. J. Santiago</strong>
    
  <a href="https://github.com/victorhjsantiago"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a><a href="URL_DO_SEU_LINKEDIN_AQUI"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>

-----------------------------------------------------------------------------------------------------------------------------
📄 Licença

Distribuído sob a Licença MIT. Veja LICENSE para mais informações.
