# 🚀 Guia de Estudos: Ecossistema Git, GitHub e CI/CD

Este repositório documenta o aprendizado consolidado sobre controle de versão, estratégias de ramificação e automação de fluxos de trabalho (CI/CD) utilizando as melhores práticas do mercado.

## 📌 Sumário
1. [Conceitos Fundamentais](#-conceitos-fundamentais)
2. [Estratégias de Branching](#-estratégias-de-branching)
3. [Comandos Essenciais](#-comandos-essenciais)
4. [GitHub Actions e Automação](#-github-actions-e-automação)
5. [Boas Práticas e Segurança](#-boas-práticas-e-segurança)
6. [Registro de Interação (Prompts)](#-registro-de-interação-prompts)

---

## 🧠 Conceitos Fundamentais

*   **Git:** Um sistema de controle de versão distribuído que permite rastrear alterações, reverter erros e colaborar de forma independente [1].
*   **GitHub:** Plataforma de hospedagem para repositórios Git que oferece ferramentas de colaboração como Pull Requests e Issues [2, 3].
*   **Branch (Ramificação):** Um ponteiro móvel para um commit específico, funcionando como um **sandbox isolado** onde alterações podem ser feitas sem afetar a linha principal (`main`) [4, 5].

---

## 🌿 Estratégias de Branching

O gerenciamento de branches é vital para a organização do time:

1.  **GitHub Flow:** Focado em deploy contínuo e rapidez. Consiste em criar uma branch, fazer commits, abrir um **Pull Request** para discussão e, após a aprovação, realizar o merge na `main` [6, 7].
2.  **Git Flow:** Um modelo mais robusto para ciclos de desenvolvimento longos. Utiliza branches com funções específicas [8, 9]:
    *   `main`: Código em produção.
    *   `develop`: Integração de novas funcionalidades.
    *   `feature`: Desenvolvimento de novas funções.
    *   `release`: Preparação para novos lançamentos oficiais.
    *   `hotfix`: Correções urgentes em produção.

---

## 🛠 Comandos Essenciais

### Gerenciamento de Ramificações
*   `git branch`: Lista as branches locais [10].
*   `git branch [nome]`: Cria uma nova branch [10].
*   `git checkout -b [nome]` ou `git switch -c [nome]`: Cria e muda para a nova branch simultaneamente [11, 12].
*   `git merge [branch]`: Combina o histórico da branch especificada com a atual [10, 13].
*   `git branch -d [nome]`: Exclui uma branch após o merge [14].

### Fluxo Diário
*   `git status`: Relatório do estado atual do repositório [15].
*   `git add [arquivo]`: Prepara as mudanças (Staging Area) [16].
*   `git commit -m "[mensagem]"`: Grava o snapshot no histórico [16].
*   **Commits Semânticos:** Uso de prefixos como `feat:`, `fix:`, `docs:`, `style:`, `refactor:`, `test:` e `chore:` para clareza no histórico [17, 18].

---

## 🤖 GitHub Actions e Automação

O **GitHub Actions** permite automatizar o pipeline de CI/CD através de arquivos **YAML** localizados em `.github/workflows/` [19, 20].

*   **Componentes:**
    *   **Workflows:** Processos automatizados disparados por **Eventos** (`push`, `pull_request`, `workflow_dispatch`) [21, 22].
    *   **Jobs:** Conjuntos de etapas executadas em um **Runner** (máquina virtual ou contêiner) [23, 24].
    *   **Steps/Actions:** Etapas individuais que executam scripts ou ações reutilizáveis do Marketplace [23, 25].
*   **Recursos Avançados:**
    *   **Matrix Strategy:** Roda o mesmo job em múltiplas versões (ex: diferentes versões de Node.js) simultaneamente [26, 27].
    *   **Secrets:** Armazenamento seguro de dados sensíveis (tokens, chaves de API), mascarados nos logs [28, 29].
    *   **Artifacts:** Persistência e transferência de arquivos entre jobs de um mesmo workflow [30, 31].

---

## 🛡 Boas Práticas e Segurança

*   **Princípio do Menor Privilégio:** Configurar permissões granulares para o `GITHUB_TOKEN` [32].
*   **Proteção de Branch:** Exigir aprovações de Pull Requests e passagens em testes automatizados antes do merge na `main` [33, 34].
*   **Higiene:** Deletar branches de feature logo após o merge para evitar poluição visual no repositório [35].
*   **OIDC:** Utilizar OpenID Connect para autenticação segura em nuvens (AWS, Azure, GCP) sem chaves estáticas [36].

---

## 💬 Registro de Interação (Prompts)

Durante o desenvolvimento deste material, foram realizados os seguintes questionamentos à IA:

1.  *"Converse sobre o que essas fontes dizem de git branch (Listar/Criar), no contexto mais amplo de Gerenciamento de Ramificações."*
2.  *"Sobre esse notebook, poderia gerar um resumo para o README.md para subir para um repositório git"*
3.  *"Como pegar esse notebooklm e colocar no github"*
4.  *"Me escreva outro README.md no formato mesmo .md, e inclui alguns prompt que realizei com você"*

---
*Este material foi gerado com base em tutoriais de especialistas e documentação oficial via NotebookLM.*
