# Projeto DevOps Fundamentals - DIO

Este repositório contém a implementação prática do desafio DevOps Fundamentals da DIO, demonstrando a criação de uma pipeline de CI/CD utilizando Microsoft Azure e Azure DevOps.

##  Arquitetura do Projeto

O projeto foi desenvolvido para provisionar uma infraestrutura na nuvem e automatizar o deploy de uma aplicação web estática.

**Principais recursos criados no Microsoft Azure:**
*   **Service Principal (App Registration):** `sp-azuredevops`
*   **Armazenamento:** Storage Account `stinfradevopsmurilo` (região Brazil South)
*   **Container Blob:** `meucontainer`

**Fluxo de CI/CD configurado no Azure DevOps:**
*   **Conexão com o Azure:** Service Connection (`azure-connection`) usando Workload Identity Federation (OIDC).
*   **Pipeline (`azure-pipelines.yml`):** Configurado para executar estágios de *Build* e *Deploy*. O estágio de *Deploy* está configurado para publicar os artefatos diretamente no `meucontainer` do Storage Account.

##  Estrutura do Repositório

*   **`/website`**: Contém os arquivos HTML estáticos que seriam utilizados como aplicação de teste.
*   **`/codigoTerraform`**: Código Terraform para provisionamento da infraestrutura no Azure.
*   **`azure-pipelines.yml`**: Pipeline principal do Azure DevOps, com os estágios de CI/CD.

##  Tecnologias Utilizadas

*   **Provedor Cloud:** Microsoft Azure
*   **Ferramenta de DevOps:** Azure DevOps (Pipelines, Repos)
*   **Infraestrutura como Código:** Terraform
*   **Controle de Versão:** Git e GitHub
