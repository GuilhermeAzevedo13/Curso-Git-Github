# 🚀 Git & GitHub: O Guia Prático

Este checklist é um guia prático baseado no seu material de estudo. A ideia é executar o comando no terminal e marcar o checkbox aqui.

---

## 🟦 Nível 1: Setup e Configuração Inicial
*Comandos: config, init, remote*

- [ ] **Tarefa 01:** Configure seu nome: `git config --global user.name "Seu Nome"`.
- [ ] **Tarefa 02:** Configure seu e-mail: `git config --global user.email "seu@email.com"`.
- [ ] **Tarefa 03:** Inicie o repositório (se ainda não fez): `git init`.
- [ ] **Tarefa 04:** Conecte ao GitHub (caso tenha criado o repo localmente primeiro): `git remote add origin URL_DO_SEU_REPO`.
- [ ] **Tarefa 05:** Verifique se tudo está certo: `git config --list`.

---

## 🟩 Nível 2: O Ciclo Básico (Git Flow, Add, Commit)
*Comandos: checkout -b, add, commit, push, status*

- [ ] **Tarefa 06 (Padrão Git Flow):** Crie antes uma branch e já entre nela com nome `develop` usando o comando `git checkout -b develop` e suba essa nova branch para o seu GitHub com `git push -u origin develop`.
- [ ] **Tarefa 07:** Crie um arquivo `index.html`. Rode `git status` para vê-lo como "Untracked".
- [ ] **Tarefa 08:** Adicione apenas este arquivo: `git add index.html`.
- [ ] **Tarefa 09:** Faça o commit: `git commit -m "Feat: Cria index.html"`.
- [ ] **Tarefa 10:** Modifique o `index.html` (adicione qualquer texto).
- [ ] **Tarefa 11:** Use o comando "combo" para adicionar e comitar de uma vez: `git commit -am "Update: Atualiza index via combo"`.
- [ ] **Tarefa 12:** Envie as alterações da develop para o GitHub: `git push`.

---

## 🟨 Nível 3: O "Ctrl+Z" do Git (Desfazendo Coisas)
*Comandos: checkout --, reset, revert, rm --cached*

- [ ] **Tarefa 13 (Desfazer alteração):** Modifique o `index.html` novamente (escreva algo errado). **Não** faça commit.
- [ ] **Tarefa 14:** Desfaça essa alteração voltando o arquivo ao estado original: `git checkout -- index.html` (ou `git restore index.html`).
- [ ] **Tarefa 15 (Ignorar arquivo):** Crie um arquivo `.env` com uma senha falsa.
- [ ] **Tarefa 16:** Adicione ele sem querer ao stage: `git add .env`.
- [ ] **Tarefa 17:** Remova ele do stage sem apagar do computador: `git rm --cached .env`. (Depois adicione ao `.gitignore`).
- [ ] **Tarefa 18 (Reset Soft):** Faça um commit qualquer. Depois, desfaça esse commit mantendo os arquivos: `git reset --soft HEAD~1`.
- [ ] **Tarefa 19 (Revert):** Faça um novo commit. Agora, crie um "anti-commit" que anula ele sem apagar o histórico: `git revert HEAD`.

---

## 🟧 Nível 4: Multitarefa com Stash
*Comandos: stash, stash list, stash pop*

*Cenário: Você está editando um arquivo, mas precisa trocar de branch urgente sem fazer commit de código incompleto.*

- [ ] **Tarefa 20:** Faça uma edição no `index.html` mas **não** faça commit.
- [ ] **Tarefa 21:** Guarde essa mudança na "gaveta": `git stash`. (O arquivo voltará ao estado anterior).
- [ ] **Tarefa 22:** Verifique o que está guardado: `git stash list`.
- [ ] **Tarefa 23:** Recupere a mudança e limpe a gaveta: `git stash pop`.

---

## 🟥 Nível 5: Branches e Manipulação de Histórico
*Comandos: branch, checkout, merge, rebase, cherry-pick*

- [ ] **Tarefa 24 (Nova Branch):** Crie e entre numa branch a partir da develop: `git checkout -b feature-teste`.
- [ ] **Tarefa 25:** Crie um arquivo `teste.txt` e faça commit na branch `feature-teste`.
- [ ] **Tarefa 26 (Cherry-Pick):** Volte para a `develop`. Copie o commit que você fez na outra branch e traga para cá sem fazer merge completo: `git cherry-pick ID_DO_COMMIT`.
- [ ] **Tarefa 27 (Rebase Interativo):** Vamos renomear um commit antigo. Rode `git rebase -i HEAD~3`.
- [ ] **Tarefa 28:** No editor que abrir, troque a palavra `pick` por `reword` no commit que deseja alterar, salve, e digite a nova mensagem.

---

### 🏆 Missão Cumprida!
Se você chegou até aqui, você praticou os comandos essenciais listados no seu guia, incluindo instalação, fluxo básico, correções de erros e manipulação avançada de histórico.
