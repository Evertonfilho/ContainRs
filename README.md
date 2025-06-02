# 🚀 Sistema de Gestão de Clientes v1.0

## 🌟 Sobre Este Projeto

Bem-vindo ao **Sistema de Gestão de Clientes**! Esta é uma aplicação web desenvolvida com **.NET MVC**, cuidadosamente arquitetada seguindo os princípios da **Clean Architecture**. O foco é fornecer uma solução robusta e organizada para as operações essenciais de gerenciamento de clientes (CRUD), garantindo uma clara separação de responsabilidades e um código mais manutenível.

---

## 🏗️ Design Arquitetural: A Escolha pela Clean Architecture

A adoção da **Clean Architecture** visa promover um design de software desacoplado, testável e independente de frameworks ou detalhes de infraestrutura. Nossa implementação organiza-se nas seguintes camadas principais:

* **`Domain` (Domínio)** 核心
    * Contém as entidades de negócio (ex: Cliente) e as interfaces que definem o núcleo das regras de negócio. É o coração da aplicação.
* **`Application` (Aplicação)** 🧠
    * Orquestra os casos de uso (operações de CRUD para clientes) e implementa as regras de negócio específicas da aplicação, utilizando as interfaces do domínio.
* **`WebAPP` (Apresentação)** 💻
    * A interface com o usuário, construída com **ASP.NET Core MVC**. Responsável por receber as requisições, interagir com a camada de Aplicação e apresentar os dados.
* **`Tests` (Testes)** 🧪
    * Abriga os testes unitários, garantindo a qualidade e o correto funcionamento das regras de negócio e componentes da aplicação.

---

## ✨ Funcionalidades Principais

* ✔️ **Cadastro Completo:** Registro de novos clientes com seus dados essenciais.
* ✔️ **Gerenciamento Total (CRUD):** Operações intuitivas para listar, visualizar detalhes, editar e excluir clientes.
* ✔️ **Validações Inteligentes:** Aplicação de regras de negócio para garantir a consistência e integridade dos dados.
* ✔️ **Interface Amigável:** Design responsivo e fácil de usar, construído com ASP.NET Core MVC.

---

## 💻 Pilha Tecnológica (Tech Stack)

* **Framework:** .NET 6 (ou superior)
* **Web:** ASP.NET Core MVC
* **ORM:** Entity Framework Core (para persistência de dados)
* **Testes:** xUnit e/ou MSTest (para a camada de testes unitários)

---

## ▶️ Como Colocar Para Rodar

Siga os passos abaixo para executar o projeto em seu ambiente local:

1.  **Clone o Repositório:**
    ```bash
    git clone [https://github.com/Evertonfilho/ContainRs.git](https://github.com/Evertonfilho/ContainRs.git)
    cd ContainRs
    ```
2.  **Configuração do Banco de Dados:**
    * Ajuste a string de conexão no arquivo `appsettings.json` (ou similar) no projeto `WebAPP` (ou no projeto principal que contém as configurações de inicialização) para apontar para sua instância de banco de dados.
3.  **Aplique as Migrations:**
    * Abra o terminal na pasta do projeto que contém seu `DbContext` e as configurações do Entity Framework Core (geralmente o projeto `WebAPP` ou um projeto de Infraestrutura/Dados) e execute:
    ```bash
    dotnet ef database update
    ```
4.  **Inicie a Aplicação:**
    * Execute o projeto principal da sua aplicação (geralmente o `WebAPP` ou o projeto ASP.NET Core):
    ```bash
    # Se estiver na raiz da solução e seu projeto WebAPP se chama, por exemplo, "ContainRs.WebApp":
    dotnet run --project ./ContainRs.WebApp/ContainRs.WebApp.csproj
    # Ou, se estiver dentro da pasta do projeto WebApp:
    # cd ./ContainRs.WebApp (ou o nome correto da pasta)
    # dotnet run
    ```
    (Ou simplesmente execute pela sua IDE, como Visual Studio, clicando com o botão direito no projeto de inicialização e selecionando "Definir como Projeto de Inicialização" e depois rodando).

---

Espero que este novo estilo e estrutura ajudem a apresentar seu projeto de forma clara e organizada!
