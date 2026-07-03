# 🍃 Spring Boot - API REST de Estudantes
Este repositório contém uma API REST básica desenvolvida em **Java** com o framework **Spring Boot** e gerenciador de dependências **Maven**. O projeto foi estruturado como uma demonstração conceitual sobre como expor endpoints REST e gerenciar modelos simples utilizando os recursos de injeção de dependência e auto-configuração do Spring.
O projeto está configurado para desenvolvimento e importação facilitada no **IntelliJ IDEA** (inclui arquivos de projeto `.idea` e `.iml`).

---
## 🚀 Funcionalidades & Endpoints
O projeto expõe uma única rota de consulta de dados de estudantes:
- **Listar Estudantes (`GET /student/list`):**
  - Retorna uma lista em formato **JSON** contendo dois estudantes pré-definidos ("Doku" e "Todoroki").
  - URL de Acesso Local: `http://localhost:8080/student/list`
---
## 📂 Estrutura do Projeto
Abaixo está o mapeamento dos principais componentes de código do projeto:
```bash
SpringBoot/
├── src/
│   └── main/
│       └── java/
│           ├── br/com/springboot/awesome/
│           │   ├── endpoint/
│           │   │   └── StudentEndPoint.java    # Controlador REST que expõe o endpoint '/student/list'
│           │   ├── model/
│           │   │   └── Student.java            # POJO representando a entidade de dados do estudante
│           │   └── start/
│           │       └── ApplicationStart.java   # Classe de entrada e inicialização do Spring Boot
│           └── Main.java                       # Script de teste console simples ("Hello world!")
├── pom.xml                                     # Definições do Maven, dependências e versão do compilador Java
├── SpringBoot.iml                              # Arquivo de configuração de módulo do IntelliJ IDEA
└── README.md                                   # Documentação do projeto
```
---
## 🛠️ Tecnologias Utilizadas
- **Java JDK (v18):** Linguagem de programação padrão do compilador.
- **Spring Boot (v1.5.3.RELEASE):** Framework para facilitação de inicialização de microsserviços.
  - **`spring-boot-starter-web`:** Starter para construção de aplicações web, incluindo RESTful, usando Spring MVC. Utiliza o Tomcat como container embutido padrão.
- **Maven:** Gerenciador de dependências e build do projeto.
---
## 💻 Como Rodar o Projeto
Certifique-se de possuir o Java JDK 18 e o Maven instalados em sua máquina.
### Opção 1: Usando uma IDE (IntelliJ IDEA, Eclipse, VS Code)
1. Importe a pasta raiz `SpringBoot` como um projeto Maven.
2. Aguarde a IDE baixar as dependências declaradas no arquivo `pom.xml`.
3. Navegue até o arquivo [ApplicationStart.java](file:///C:/Users/TALITA%20CASTRO/.gemini/antigravity/scratch/SpringBoot/src/main/java/br/com/springboot/awesome/start/ApplicationStart.java).
4. Clique no botão de **Run** (Executar) ao lado do método `main`.
5. O console iniciará o servidor Tomcat embutido na porta `8080`.
6. Abra seu navegador ou ferramenta de testes (como Postman/Insomnia) e acesse: `http://localhost:8080/student/list`
### Opção 2: Pelo Terminal via Maven wrapper / comando
1. Abra o terminal na pasta raiz do projeto.
2. Execute o comando Maven para rodar a aplicação Spring Boot:
   ```bash
   mvn spring-boot:run
   ```
3. Acesse o endpoint no navegador: [http://localhost:8080/student/list](http://localhost:8080/student/list)
