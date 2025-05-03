# 💨 Air Quality Monitoring System

**Monitore a qualidade do ar com esta solução completa e containerizada\!**

Este sistema oferece uma plataforma robusta e intuitiva para o acompanhamento da qualidade do ar, integrando um backend poderoso em Python (FastAPI), um frontend dinâmico construído com Vue.js 3 e um banco de dados MySQL para armazenamento eficiente. Graças à containerização com Docker, a implantação e o gerenciamento tornam-se incrivelmente simples.

## 📑 Índice

  - [✨ Visão Geral](#visão-geral)
  - [🛠️ Pré-requisitos](#pré-requisitos)
  - [🚀 Primeiros Passos](#primeiros-passos)
  - [🌐 Acesso aos Serviços](#acesso-aos-serviços)
  - [ℹ️ Informações Importantes](#informações-importantes)
    
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
    git clone https://github.com/FernandesLP/CPID_Atividade_DevOps.git
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

  - **Backend API (FastAPI)**: Acesse a API através do seu navegador ou de uma ferramenta como Postman em `http://localhost:18003`
  - **Frontend Web (Vue.js)**: A interface web estará disponível em `http://localhost:3000`
  - **Banco de Dados (MySQL)**: O MySQL estará rodando na porta `3306` do seu localhost.

## ℹ️ Informações Importantes

  - **Banco de Dados MySQL:** O container do MySQL é configurado com as seguintes credenciais padrão:
      - **Usuário Root:** `root` (senha: `root`)
      - **Banco de Dados:** `airquality`
      - **Usuário:** `devops` (senha: `password123`)
  - **Inicialização do Banco de Dados:** O arquivo `CPID-DevOps-AirQuality-DB/AirQuality-2025-03-28-09-40-01.sql` será executado automaticamente na primeira vez que o container do MySQL for iniciado, criando a estrutura inicial do banco de dados.
  - **Variáveis de Ambiente:** As informações de conexão com o banco de dados (hostname, porta, nome do banco, usuário e senha) para o backend são declaradas diretamente no arquivo `docker-compose.yml` através da seção `environment` do serviço `backend`. Optei por esta abordagem em vez de utilizar um arquivo `.env` devido a problemas de acesso que foram identificados pelo backend em algumas configurações.
  - **Volumes:** Um volume Docker chamado `mysql_data` é utilizado para persistir os dados do banco de dados, garantindo que os dados não sejam perdidos entre reinicializações dos containers. O código do backend também é montado dentro do container para facilitar o desenvolvimento (embora neste cenário de imagens prontas, isso seja mais para inspeção).
  - **Rede Docker:** Uma rede Docker chamada `airquality` é criada para permitir a comunicação entre os containers do backend, frontend e banco de dados.
  - **Healthcheck do MySQL:** O container do MySQL possui um healthcheck configurado para garantir que o serviço esteja pronto antes que outros serviços dependentes (como o backend) tentem se conectar.
  - **Encerrando a Aplicação:** Para interromper e remover todos os containers definidos no `docker-compose.yml`, utilize o seguinte comando no mesmo diretório do arquivo:
    ```bash
    docker-compose down
    ```
    Este comando encerra graciosamente todos os serviços em execução.
  - **Verificando o Status dos Serviços:** Para verificar se todos os containers foram iniciados corretamente e estão rodando sem problemas, você pode usar o seguinte comando:
    ```bash
    docker-compose ps
    ```
    Este comando exibe o status de cada container definido no `docker-compose.yml`, indicando se estão ativos, há quanto tempo estão rodando e as portas que estão sendo expostas.
 
## Observação sobre o Desenvolvimento

É importante ressaltar que a arquitetura e implementação das funcionalidades do **backend** e do **frontend** foram responsabilidade dos orientadores desta atividade. Minha contribuição específica se concentrou na **containerização da aplicação utilizando Docker**, o que envolveu a criação e configuração do arquivo `docker-compose.yml` para orquestrar os diferentes serviços (banco de dados, backend e frontend) em containers isolados e interconectados.

Essa distinção é crucial para entender o escopo do meu trabalho, que se focou em garantir um ambiente de execução consistente e gerenciável para a aplicação desenvolvida pelos orientadores.


