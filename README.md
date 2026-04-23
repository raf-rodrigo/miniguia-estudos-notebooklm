Ecossistema Git & GitHub: Do Versionamento à Automação (CI/CD)
Este repositório reúne conhecimentos essenciais sobre o uso do Git para controle de versão e do GitHub para colaboração e automação de fluxos de trabalho.
🚀 Conceitos Fundamentais
Git: Um sistema de controle de versão distribuído que permite rastrear alterações, reverter mudanças e colaborar de forma eficiente
.
GitHub: Plataforma de hospedagem que funciona como uma biblioteca online para colaboração em projetos
.
Branch (Ramificação): Funciona como um sandbox isolado ou um ponteiro móvel para um commit, permitindo alterar o código sem afetar a linha principal (main)
.
🛠️ Comandos Essenciais (Cheat Sheet)
Configuração: git config --global user.name "[nome]" e user.email "[email]"
.
Repositórios: git init (inicializar) ou git clone [url] (copiar existente)
.
Fluxo de Trabalho:
git status: Lista arquivos modificados
.
git add [arquivo]: Prepara as mudanças (Staging Area)
.
git commit -m "[mensagem]": Grava o snapshot permanentemente
.
git push: Envia os commits para o repositório remoto
.
Gerenciamento de Branches:
git branch: Lista as branches locais
.
git branch [nome]: Cria uma nova branch
.
git checkout -b [nome] ou git switch -c [nome]: Cria e muda para a nova branch simultaneamente
.
git merge [branch]: Combina o histórico da branch especificada com a atual
.
📑 Estratégias de Branching
GitHub Flow: Fluxo leve focado em implantações rápidas e regulares. Baseia-se em branches de curta duração, Pull Requests e deploy imediato após o merge na main
.
Git Flow: Modelo robusto para ciclos de desenvolvimento longos ou múltiplos lançamentos. Utiliza branches específicas: main (produção), develop (integração), feature, release e hotfix
.
🤖 Automação com GitHub Actions
O GitHub Actions permite automatizar processos (CI/CD) através de Workflows definidos em arquivos YAML no diretório .github/workflows/
.
Componentes:
Eventos (Triggers): Gatilhos como push, pull_request ou workflow_dispatch (manual)
.
Jobs: Conjunto de etapas executadas em um Runner (servidor virtual)
.
Steps/Actions: Etapas individuais que executam scripts ou ações reutilizáveis da comunidade (Marketplace)
.
Recursos Avançados:
Secrets: Armazenamento seguro de dados sensíveis (tokens, senhas) que são mascarados nos logs
.
Matrix Strategy: Execução simultânea em várias versões de linguagem ou sistemas operacionais
.
Artifacts & Caching: Persistência de dados entre jobs e aceleração de builds através do cache de dependências
.
🛡️ Boas Práticas
Commits Semânticos: Usar prefixos como feat:, fix:, docs: para clareza no histórico
.
Segurança: Utilizar OIDC para autenticação em nuvem (sem chaves estáticas) e seguir o princípio do privilégio mínimo para o GITHUB_TOKEN
.
Higiene do Repositório: Deletar branches de funcionalidade logo após o merge para evitar poluição
.
