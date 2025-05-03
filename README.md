# 💨 Air Quality Monitoring System

![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white)

Sistema completo para o monitoramento da qualidade do ar, integrando um backend robusto em Python (FastAPI), um frontend dinâmico construído com Vue.js 3 e um banco de dados MySQL para armazenamento eficiente. A solução é totalmente containerizada utilizando Docker, facilitando a implantação e o gerenciamento.

## 📑 Índice
- [Visão Geral](#visão-geral)
- [Pré-requisitos](#pré-requisitos)
- [Primeiros Passos](#primeiros-passos)
- [Acesso aos Serviços](#acesso-aos-serviços)
- [Informações Importantes](#informações-importantes)
- [Estrutura do Projeto](#estrutura-do-projeto)

## 🧐 Visão Geral
Este sistema oferece uma solução completa para o acompanhamento da qualidade do ar, compreendendo:

- **⚙️ Backend API**: Desenvolvido em Python utilizando o framework FastAPI, proporcionando uma API rápida e eficiente para comunicação com o frontend e manipulação dos dados.
- **🌐 Frontend Web**: Interface de usuário intuitiva e reativa construída com Vue.js 3, permitindo a visualização dos dados de qualidade do ar em tempo real e o gerenciamento do sistema.
- **💾 Database**: Banco de dados MySQL 8.0, escolhido pela sua confiabilidade e escalabilidade para armazenar os dados coletados e as informações do sistema.
- **🐳 Containerização**: Todo o sistema é containerizado com Docker, simplificando a instalação, configuração e implantação em diferentes ambientes.

## 🛠️ Pré-requisitos
Antes de iniciar, certifique-se de ter as seguintes ferramentas instaladas em sua máquina:

- **Docker**: Plataforma de containerização. Você pode instalá-lo seguindo as instruções em [https://docs.docker.com/get-docker/](https://docs.docker.com/get-docker/).
- **Docker Compose**: Ferramenta para definir e gerenciar aplicações Docker multi-container. Geralmente instalado junto com o Docker Desktop ou pode ser instalado separadamente conforme as instruções em [https://docs.docker.com/compose/install/](https://docs.docker.com/compose/install/).
- **Git**: Sistema de controle de versões distribuído. Para instalar, siga as instruções em [https://git-scm.com/download](https://git-scm.com/download).

## 🚀 Primeiros Passos

Siga estas etapas para executar o sistema em sua máquina:

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/FernandesLP/CPID_Atividade_DevOps.git](https://github.com/FernandesLP/CPID_Atividade_DevOps.git)
   cd CPID_Atividade_DevOps
   
2. Acesso aos Serviços
#!/bin/bash

echo "▶️ Iniciando containers Docker..."
docker-compose up -d

echo ""
echo "✅ Serviços iniciados com sucesso!"
echo "   As imagens dos containers foram obtidas diretamente do Docker Hub."
echo "   Não é necessário realizar um build local."
echo ""

echo "🌐 Endpoints disponíveis:"
echo "   - Frontend:     http://localhost:3000"
echo "   - Backend (API): http://localhost:18003/docs"
echo "   - MySQL:        porta 3306"
echo ""
