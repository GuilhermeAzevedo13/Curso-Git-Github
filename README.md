# 🚀 Git & GitHub: O Guia Prático

Este checklist é um guia prático baseado no seu material de estudo. A ideia é executar o comando no terminal e marcar o checkbox aqui.

---

## 📚 Cheat Sheet: Padrões Adotados
*Consulte aqui antes de fazer as tarefas.*

### 🏷️ Tipos de Commit (Semantic Commits)
| Tipo | Quando usar | Exemplo |
| :--- | :--- | :--- |
| **feat** | Nova funcionalidade para o usuário. | `feat: add login button` |
| **fix** | Correção de bug. | `fix: resolve validation error` |
| **docs** | Alteração apenas na documentação. | `docs: update readme instructions` |
| **style** | Formatação, pontos e vírgulas (sem mudar lógica). | `style: format css indentation` |
| **refactor** | Melhoria de código que não muda a funcionalidade. | `refactor: simplify auth logic` |
| **chore** | Atualização de tarefas de build, configs, ferramentas. | `chore: update npm packages` |
| **test** | Adição ou correção de testes. | `test: add unit test for user service` |

### 🌿 Nomes de Branches (Git Flow)
| Branch | Padrão de Nome | Finalidade |
| :--- | :--- | :--- |
| **Feature** | `feature/nome-da-feature` | Desenvolver algo novo. Sai da `develop`. |
| **Hotfix** | `hotfix/nome-do-erro` | Correção urgente. Sai da `main`. |
| **Release** | `release/v1.0.0` | Preparação para versão final. |

---

## 🟦 Nível 1: Setup e Configuração Inicial
*Comandos: config, init, remote*

- [ ] **Tarefa 01:** Configure seu nome: `git config --global user.name "Seu Nome"`.
- [ ] **Tarefa 02:** Configure seu e-mail: `git config --global user.email "seu@email.com"`.
- [ ] **Tarefa 03:** Conecte ao GitHub (caso tenha criado o repo localmente primeiro): `git remote add origin URL_DO_SEU_REPO`.
- [ ] **Tarefa 04:** Verifique se tudo está certo: `git config --list`.
- [ ] **Tarefa 05:** Essa parte é **OPCIONAL** caso nao prefira a Tarefa 05 -> Realize o Fork desse repositório para o seu GitHub
- [ ] **Tarefa 06:** Pegue a URL SSH desse repositório para clonar em sua máquina local e digite no terminal de sua máquina: `git clone URL_SSH_DO_SEU_REPO`

---

## 🟩 Nível 2: O Ciclo Básico (Git Flow, Add, Commit)
*Comandos: checkout -b, add, commit, push, status*

- [ ] **Tarefa 07 (Padrão Git Flow):** Crie antes uma branch e já entre nela com nome `develop` usando o comando `git checkout -b develop` e suba essa nova branch para o seu GitHub com `git push -u origin develop`.
- [ ] **Tarefa 08:** Crie outra branch dentro da branch `develop` com o nome `feature/criar-index`.
- [ ] **Tarefa 09:** Crie um arquivo `index.html`. Rode `git status` para vê-lo como "Untracked".
- [ ] **Tarefa 10:** Adicione apenas este arquivo: `git add index.html`.
- [ ] **Tarefa 11:** Faça o commit: `git commit -m "Feat: Cria index.html"`.
- [ ] **Tarefa 12:** Modifique o `index.html` (adicione qualquer texto).
- [ ] **Tarefa 13:** Use o comando "combo" para adicionar e comitar de uma vez: `git commit -am "Update: Atualiza index via combo"`.
- [ ] **Tarefa 14:** Envie as alterações da develop para o GitHub: `git push origin feature/criar-index`.
- [ ] **Tarefa 15:** Vá para o GitHup e na página do Repositório e crie um Pull Request e faça o merge e apague a branch `feature/criar-index` no GitHub e no repositório local de sua máquina faça o checkout para a branch `develop` e em seguida apague a branch `feature/criar-index` do seu repositório local com git branch -d `feature/criar-index`.

---

## 🟨 Nível 3: O "Ctrl+Z" do Git (Desfazendo Coisas)
*Comandos: checkout --, reset, revert, rm --cached*

- [ ] **Tarefa 16 (Desfazer alteração):** Modifique o `index.html` novamente (escreva algo errado). **Não** faça commit.
- [ ] **Tarefa 17:** Desfaça essa alteração voltando o arquivo ao estado original: `git checkout -- index.html` (ou `git restore index.html`).
- [ ] **Tarefa 18 (Commit Chore):** Crie um arquivo `.gitignore` (pode deixar vazio por enquanto). Faça o commit usando o padrão:
    - Mensagem: `git commit -m "chore: create gitignore file"`
- [ ] **Tarefa 19 (Ignorar arquivo):** Crie um arquivo `.env` com uma senha falsa.
- [ ] **Tarefa 20:** Adicione ele sem querer ao stage: `git add .env`.
- [ ] **Tarefa 21:** Remova ele do stage sem apagar do computador: `git rm --cached .env`. (Depois adicione ao `.gitignore`).
- [ ] **Tarefa 22 (Reset Soft):** Faça um commit qualquer. Depois, desfaça esse commit mantendo os arquivos: `git reset --soft HEAD~1`.
- [ ] **Tarefa 23 (Revert):** Faça um novo commit. Agora, crie um "anti-commit" que anula ele sem apagar o histórico: `git revert HEAD`.

---

## 🟧 Nível 4: Multitarefa com Stash
*Comandos: stash, stash list, stash pop*

*Cenário: Você está editando um arquivo, mas precisa trocar de branch urgente sem fazer commit de código incompleto.*

- [ ] **Tarefa 24:** Faça uma edição no `index.html` mas **não** faça commit.
- [ ] **Tarefa 25:** Guarde essa mudança na "gaveta": `git stash`. (O arquivo voltará ao estado anterior).
- [ ] **Tarefa 26:** Verifique o que está guardado: `git stash list`.
- [ ] **Tarefa 27:** Recupere a mudança e limpe a gaveta: `git stash pop`.

---

## 🟥 Nível 5: Branches e Manipulação de Histórico
*Comandos: branch, checkout, merge, rebase, cherry-pick*

- [ ] **Tarefa 28 (Nova Branch):** Crie e entre numa branch a partir da develop: `git checkout -b feature-teste`.
- [ ] **Tarefa 29:** Crie um arquivo `teste.txt` e faça commit na branch `feature-teste`.
- [ ] **Tarefa 30 (Cherry-Pick):** Volte para a `develop`. Copie o commit que você fez na outra branch e traga para cá sem fazer merge completo: `git cherry-pick ID_DO_COMMIT`, DICA: Use `git log` .
- [ ] **Tarefa 31 (Rebase Interativo):** Vamos renomear um commit antigo. Rode `git rebase -i HEAD~3`.
      OBS.:  **rebase**: "Reescrever a base" ou o histórico.
            **-i (interactive)**: Modo interativo: Ele vai abrir um editor de texto para perguntar o que você quer fazer com cada commit;
             **HEAD~3**: Significa "pegue os últimos 3 commits a partir de agora", 
- [ ] **Tarefa 32:** No editor que abrir, troque a palavra `pick` por `reword` no commit que deseja alterar, salve, e digite a nova mensagem.
      OBS.: Por padrão, todos vêm como pick.
            - pick: Significa "Mantenha esse commit exatamente como ele é".
            - reword: Significa "Mantenha o código, mas deixe-me reescrever a mensagem desse commit".
            - drop: Significa "Apague esse commit e o código dele da existência".
            - squash: Significa "Funda esse commit com o anterior" (juntar dois em um).
      O Git vai abrir o editor novamente, mas agora mostrando apenas a mensagem daquele commit que você marcou como reword.
      Apague o texto antigo ("fix: arruma botao torto") e escreva o novo ("fix: arrumar dois botoes tortos").

      ⚠️ CUIDADO COM O REBASE
      Nunca faça rebase em commits que você já subiu para o GitHub (push) e que outras pessoas estão usando. Mudar o histórico de uma branch compartilhada (como a develop ou main) quebra o código dos colegas. Use o rebase livremente apenas nas suas branches de feature locais ou antes de dar o push.
---

## 🟧 Nível Extra: Hotfix (Correção Urgente) -- (OPCIONAL)
*Foco: Simular um erro em produção (main).*

- [ ] **Tarefa 33 (Troca de Contexto):** Volte para a branch `main`: `git checkout main`.
- [ ] **Tarefa 34 (Simulação):** Suponha que acharam um erro crítico. Crie uma branch de hotfix a partir da main:
    - Comando: `git checkout -b hotfix/fix-critical-README`
- [ ] **Tarefa 35 (Correção):** Crie/Edite um arquivo `README.md` corrigindo o "erro" que seria marcar um X nas tarefas que vc ja realizou.
- [ ] **Tarefa 36 (Commit Fix):** Comite a correção:
    - Mensagem: `fix: adicionado X nos topicos da Tarefa Y que realizei`
- [ ] **Tarefa 37 (Merge):** Volte para a main e faça o merge do hotfix.
    - `git checkout main`
    - `git merge hotfix/fix-critical-header`
    - (Opcional) Delete a branch: `git branch -d hotfix/fix-critical-header`

---

### 🏆 Missão Cumprida!
Se você chegou até aqui, você praticou os comandos essenciais listados no seu guia, incluindo instalação, fluxo básico, correções de erros e manipulação avançada de histórico.
