# Organice
### By: Pedro Pertusi & João Alfredo Lamy

## Descrição Geral

O Organice é um sistema de agenda que imita as funcionalidades conhecidas do Notion, permitindo aos usuários criar lembretes e visualizar dias e semanas. Com funcionalidades adicionais de ativação de notificações para o WhatsApp, o Organice oferece uma experiência robusta e interativa para gerenciamento de tempo e tarefas.

## Microserviços

A arquitetura do Organice é baseada em microserviços, cada um com sua responsabilidade única dentro do sistema. Abaixo estão os microserviços que compõem o sistema:

### [organice-gateway](https://github.com/alfredjynx/organice-gateway.git)
Gateway padrão do sistema, encarregado de rotear as requisições para os microserviços apropriados.

### [organice-docker-api](https://github.com/alfredjynx/organice-docker-api.git)
Repositório com as configurações do Docker para a orquestração dos containers do sistema Organice.

### [organice-discovery](https://github.com/alfredjynx/organice-discovery.git)
Serviço responsável pelo registro e descoberta dos microserviços, possibilitando a comunicação interna eficiente.

### [organice-ops](https://github.com/alfredjynx/organice-ops.git)
Repositório com as configurações do Jenkins.

### Autenticação
- [organice-auth](https://github.com/alfredjynx/organice-auth.git): Serviço para autenticação de usuários, incluindo login e geração de tokens de acesso.
- [organice-auth-resource](https://github.com/alfredjynx/organice-auth-resource.git): Contém os recursos associados ao serviço de autenticação.

### Contas
- [organice-account](https://github.com/alfredjynx/organice-account.git): Gerencia a criação e listagem de contas de usuários.
- [organice-account-resource](https://github.com/alfredjynx/organice-account-resource.git): Fornece os recursos para o serviço de contas.

### Lembretes
- [organice-lembrete](https://github.com/alfredjynx/organice-lembrete.git): Permite a criação e listagem de lembretes, integrando-os ao sistema de agenda.
- [organice-lembrete-resource](https://github.com/alfredjynx/organice-lembrete-resource.git): Oferece os recursos relacionados aos lembretes.

### Dias
- [organice-dia](https://github.com/PedroPertusi/organice-dia.git): Permite a criação e listagem de dias, integrando-os ao sistema de agenda.
- [organice-dia-resource](https://github.com/PedroPertusi/organice-dia-resource.git): Oferece os recursos relacionados aos dias.

## Instruções de Instalação e Execução

Para facilitar a instalação e execução dos serviços, utilize o Docker e o Docker Compose seguindo os passos abaixo.

### Pré-requisitos

Certifique-se de que você tenha instalado:
- Docker
- Docker Compose
- Java JDK (versão recomendada: 11 ou superior)
- Apache Maven

### Executando os serviços com Docker

1. Clone o repositório `organice-docker-api`:

```bash
git clone https://github.com/alfredjynx/organice-docker-api.git
