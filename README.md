# 🚀 Git & GitHub: O Guia Prático

Este checklist foi desenhado para praticar o fluxo de trabalho real de um desenvolvedor, desde a configuração inicial até a colaboração via Pull Requests.

Faça o commit dessa mudança: git commit -am "Progress: Tarefa 01 concluída".

Repita para a próxima.

---

## 🟦 Módulo 1: Setup e Primeiros Passos
*Baseado na seção: Instalação, SSH e Configuração*

- [ ] **Tarefa 01 (Verificação):** Abra seu terminal e verifique se o Git está instalado rodando `git --version`.
- [ ] **Tarefa 02 (Identidade):** Configure seu nome de usuário: `git config --global user.name "Seu Nome"`.
- [ ] **Tarefa 03 (Identidade):** Configure seu e-mail (o mesmo do GitHub): `git config --global user.email "seu@email.com"`.
- [ ] **Tarefa 04 (SSH):** Verifique se você possui uma chave SSH configurada ou crie uma nova para conectar ao GitHub sem senha.
- [ ] **Tarefa 05 (Check):** Rode `git config --list` e confira se seus dados aparecem corretamente.

---

## 🟦 Módulo 2: O Ciclo de Vida do Código
*Baseado na seção: Comandos Básicos, Repositórios e Commits*

- [ ] **Tarefa 06 (Status):** Crie um arquivo chamado `conceitos.txt` e escreva uma frase sobre o que é Git. Rode `git status` para ver o arquivo como "Untracked".
- [ ] **Tarefa 07 (Staging):** Adicione o arquivo à área de preparação com `git add conceitos.txt`.
- [ ] **Tarefa 08 (Commit):** Faça o commit com uma mensagem clara: `git commit -m "Docs: Adiciona definição inicial de Git"`.
- [ ] **Tarefa 09 (Log):** Visualize o histórico do que foi feito até agora com `git log`.
- [ ] **Tarefa 10 (Sincronia):** Envie suas alterações para o repositório remoto (GitHub) com `git push`.

---

## 🟦 Módulo 3: Trabalhando com Branches
*Baseado na seção: Branches (Criar, Trocar e Merge)*

- [ ] **Tarefa 11 (Criar):** Crie uma nova branch para desenvolver uma nova funcionalidade: `git branch feature-logs`.
- [ ] **Tarefa 12 (Trocar):** Mude para essa nova branch: `git switch feature-logs` (ou `git checkout feature-logs`).
- [ ] **Tarefa 13 (Modificar):** Crie um novo arquivo chamado `logs.txt`, adicione conteúdo, faça o `git add . ou git add lods.txt` e o `git commit`.
- [ ] **Tarefa 14 (Voltar):** Volte para a branch principal (`main` ou `master`) com `git checkout main`.
- [ ] **Tarefa 15 (Verificar):** Observe que o arquivo `logs.txt` sumiu (pois ele só existe na outra branch).
- [ ] **Tarefa 16 (Merge):** Estando na `main`, junte o trabalho feito na outra branch: `git merge feature-logs`.
- [ ] **Tarefa 17 (Limpeza):** Delete a branch antiga que não é mais necessária: `git branch -d feature-logs`.

---

## 🟦 Módulo 4: GitHub Flow (Colaboração Real)
*Baseado na seção: Fork, Pull Request (PR) e Issues*

> **Nota:** Para estas tarefas, você usará a interface web do GitHub junto com o terminal.

- [ ] **Tarefa 18 (Issues):** Vá na aba **Issues** do seu repositório no GitHub, clique em "New Issue" e crie um ticket com o título: "Bug: Corrigir erro de digitação no README".
- [ ] **Tarefa 19 (Branch de Correção):** No terminal, crie uma branch específica para essa tarefa: `git checkout -b fix-readme`.
- [ ] **Tarefa 20 (Ação):** Faça uma pequena alteração neste README (pode ser marcar este checkbox!), adicione e comite.
- [ ] **Tarefa 21 (Push da Branch):** Envie essa branch nova para o GitHub: `git push origin fix-readme`.
- [ ] **Tarefa 22 (Pull Request):** No GitHub, aparecerá um botão "Compare & pull request". Clique nele.
- [ ] **Tarefa 23 (Linkar Issue):** Na descrição do PR, escreva "Closes #1" (onde #1 é o número da Issue que você criou na Tarefa 18). Isso fecha a issue automaticamente.
- [ ] **Tarefa 24 (Merge via Web):** Aprove seu próprio PR (ou faça o "Merge Pull Request") pela interface do GitHub.
- [ ] **Tarefa 25 (Sincronizar Local):** De volta ao terminal, na branch `main`, puxe as atualizações que foram aceitas no GitHub: `git pull`.

---

### 🎉 Parabéns!
Se você marcou todos os itens acima, você executou o ciclo completo de desenvolvimento de software moderno: **Configuração -> Desenvolvimento Local -> Branching -> Merge Local -> Pull Request -> Deploy na Main.**
