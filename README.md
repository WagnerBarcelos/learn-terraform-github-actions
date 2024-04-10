# Automatizando Terraform com GitHub Actions

## Resumo

Esse documento aborda a integração do Terraform Cloud com GitHub Actions para automação de workflows de CI/CD. Utilizando as GitHub Actions fornecidas pela HashiCorp, é possível criar workflows personalizados de CI/CD que se integram à API do Terraform Cloud, permitindo uma automação avançada e customizada para os processos de planejamento, aplicação e destruição de configurações do Terraform.

### Objetivos do Tutorial

- **Automatizar o Terraform com CI/CD:** Usar o GitHub Actions para integrar a automação do Terraform em repositórios do GitHub.
- **Workflow Personalizado:** Criar um workflow de CI/CD personalizado que se integra com o Terraform Cloud para implantação de um servidor web acessível publicamente.

### Pré-requisitos

- Familiaridade com Terraform e Terraform Cloud.
- Contas no GitHub, Terraform Cloud e AWS.

### Configuração Inicial

1. **Configurar o Terraform Cloud:**
   - Criar um workspace chamado `learn-terraform-github-actions`.
   - Adicionar credenciais da AWS como variáveis de ambiente.
   - Gerar um token de usuário API do Terraform Cloud.

2. **Configurar um Repositório GitHub:**
   - Usar um template fornecido para criar um novo repositório.
   - Adicionar o token API do Terraform Cloud como um segredo no repositório.

### Fluxo de Trabalho com GitHub Actions

1. **Terraform Plan:**
   - Gerar um plano para cada commit em um branch de pull request para revisão no Terraform Cloud.
   - Utilizar o arquivo `.github/workflows/terraform-plan.yml` para definir este workflow.

2. **Terraform Apply:**
   - Aplicar a configuração ao atualizar o branch principal.
   - Definir este processo no arquivo `.github/workflows/terraform-apply.yml`.

### Testando o Workflow

- Criar e mesclar um pull request para testar o workflow completo.
- Verificar a criação dos recursos e a acessibilidade pública do servidor web provisionado.

### Limpeza

- Destruir os recursos e excluir o workspace do Terraform Cloud após os testes para evitar cobranças.

### Próximos Passos

- O tutorial encoraja a personalização do workflow de GitHub Actions para adaptá-lo às necessidades específicas da organização.

## Conclusão

Automatizar o Terraform com GitHub Actions proporciona um processo de integração contínua robusto, promove melhores práticas de configuração e colaboração entre as equipes e automatiza o fluxo de trabalho do Terraform, aumentando a eficiência e a confiabilidade da gestão de infraestrutura como código.

