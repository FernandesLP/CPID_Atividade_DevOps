# 💨 Air Quality Monitoring System

**Monitore a qualidade do ar com esta solução completa e containerizada\!**

Este sistema oferece uma plataforma robusta e intuitiva para o acompanhamento da qualidade do ar, integrando um backend poderoso em Python (FastAPI), um frontend dinâmico construído com Vue.js 3 e um banco de dados MySQL para armazenamento eficiente. Graças à containerização com Docker, a implantação e o gerenciamento tornam-se incrivelmente simples.

## 📑 Índice

  - [✨ Visão Geral](#visão-geral)
  - [🛠️ Pré-requisitos](#pré-requisitos)
  - [🚀 Primeiros Passos](#primeiros-passos)
  - [🌐 Acesso aos Serviços](#acesso-aos-serviços)
    
## ✨ Visão Geral

Este sistema é uma solução completa para o monitoramento da qualidade do ar, abrangendo:

  - **⚙️ Backend API**: Desenvolvido em Python com o framework FastAPI, oferecendo uma API de alta performance para a comunicação com o frontend e a manipulação dos dados de qualidade do ar.
  - **🌐 Frontend Web**: Uma interface de usuário moderna e reativa construída com Vue.js 3, permitindo a visualização em tempo real dos dados de qualidade do ar e o gerenciamento do sistema de forma intuitiva.
  - **💾 Database**: Banco de dados MySQL 8.0, escolhido por sua confiabilidade e escalabilidade para armazenar os dados coletados e as informações do sistema de maneira eficiente.
  - **🐳 Containerização**: Todo o sistema é empacotado em containers Docker, simplificando drasticamente a instalação, configuração e implantação em qualquer ambiente que suporte Docker.

## 🛠️ Pré-requisitos

Antes de começar, certifique-se de ter as seguintes ferramentas instaladas em sua máquina:

  - **Docker**: A plataforma líder para containerização. Instale seguindo as instruções em [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/).
  - **Docker Compose**: Uma ferramenta essencial para definir e gerenciar aplicações Docker multi-container. Geralmente é instalado junto com o Docker Desktop ou pode ser instalado separadamente conforme as instruções em [https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/).
  - **Git**: O sistema de controle de versões distribuído. Para instalar, siga as instruções em [https://git-scm.com/download](https://git-scm.com/download).

## 🚀 Primeiros Passos

Siga estas etapas para colocar o sistema em funcionamento na sua máquina:

1.  **Clone o repositório:**

    ```bash
    git clone [https://github.com/FernandesLP/CPID_Atividade_DevOps.git](https://github.com/FernandesLP/CPID_Atividade_DevOps.git)
    ```

2.  **Navegue até o diretório do projeto:**

    ```bash
    cd CPID_Atividade_DevOps
    ```

3.  **Execute o sistema com Docker Compose:**
    Como as imagens já estão hospedadas no Docker Hub, você pode iniciar todos os serviços (backend, frontend e banco de dados) com um único comando, sem a necessidade de construir as imagens localmente.

    ```bash
    docker-compose up -d
    ```

    Este comando fará com que o Docker Compose baixe as imagens `fernandeslp/cpid-backend:1.0.0` e `fernandeslp/cpid-frontend:1.0.0` do Docker Hub, além de utilizar a imagem oficial do MySQL 8.0. O arquivo `docker-compose.yml` dentro do repositório já está configurado para orquestrar esses serviços.

## 🌐 Acesso aos Serviços

Após a execução do `docker-compose up -d`, os seguintes serviços estarão acessíveis:

  - **Backend API (FastAPI)**: Acesse a API através do seu navegador ou de uma ferramenta como Postman em `http://localhost:18003`.
  - **Frontend Web (Vue.js)**: A interface web estará disponível em `http://localhost:3000`.
  - **Banco de Dados (MySQL)**: O MySQL estará rodando na porta `3306` do seu localhost, embora geralmente você interaja com ele através do backend.
