# Guia de Bolso Ilustrado de Git

Um guia visual de consulta rápida em página única (`index.html`) sobre as operações mais usadas do Git, com diagramas interativos que mostram como cada comando afeta commits, branches e áreas do repositório.

## Sobre o Projeto

Este projeto reúne explicações diretas, exemplos práticos de linha de comando e diagramas visuais (usando **Mermaid `gitGraph`** e esquemas em HTML/CSS) para facilitar o entendimento do fluxo de trabalho no Git — desde os conceitos fundamentais até resolução de conflitos e sincronização com repositórios remotos.

## Conteúdo Abordado

### 1. Fundamentos
- **`git init`** — Inicialização de repositório e visão das três áreas do Git (*Working Directory*, *Staging* e *Repositório*).
- **`git clone`** — Cópia completa de um repositório remoto.
- **`git status`** — Inspeção do estado atual dos arquivos e da branch.
- **`git add`** — Preparação de alterações na área de *Staging*.
- **`git commit`** — Gravação de mudanças no histórico.
- **`git log`** — Visualização do histórico de commits.

### 2. Branches e Integração
- **`git branch`** — Criação, listagem e remoção de branches.
- **`git checkout` / `git switch`** — Troca de branch ativa (`HEAD`).
- **`git merge`** — União do histórico de duas branches.
- **Conflitos de merge** — Como identificar marcadores de conflito (`<<<<<<<`, `=======`, `>>>>>>>`) e passo a passo para resolvê-los.
- **`git rebase`** — Reaplicação de commits sobre outra base para manter o histórico linear (com comparativo *Antes / Depois*).
- **`git cherry-pick`** — Cópia pontual de um commit específico para a branch atual.

### 3. Desfazer e Reverter
- **`git reset`** — Recuo do ponteiro da branch e diferenças entre `--soft`, `--mixed` e `--hard`.
- **`git revert`** — Criação de um commit reverso para desfazer mudanças de forma segura em branches compartilhadas.
- **`git stash`** — Armazenamento temporário de alterações em andamento.

### 4. Trabalhando com Remoto
- **`git fetch`** — Atualização de referências remotas sem alterar branches locais.
- **`git pull`** — Busca e integração imediata (`fetch` + `merge` ou `rebase`).
- **`git push`** — Envio de commits locais para o repositório remoto.

## Como Usar

O projeto não requer instalação de dependências nem servidor de build:

1. Clone ou baixe este repositório:
   ```bash
   git clone <url-do-repositorio>
   cd guia-ilustrado-git
   ```
2. Abra o arquivo `index.html` diretamente em qualquer navegador moderno.

### Uso 100% Offline

Por padrão, o `index.html` carrega a biblioteca [Mermaid](https://mermaid.js.org/) via CDN (`jsdelivr`) para renderizar os grafos de commits. Caso queira utilizar o guia sem conexão com a internet:

1. Baixe o arquivo [`mermaid.min.js`](https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.min.js) e salve-o na mesma pasta do `index.html`.
2. No final do arquivo `index.html`, substitua a tag `<script>` do CDN por:
   ```html
   <script src="mermaid.min.js"></script>
   ```

## Tecnologias Utilizadas

- **HTML5 & CSS3** — Layout responsivo, variáveis CSS, índice navegável fixo (*sticky TOC*) e diagramas das áreas do Git.
- **[Mermaid.js](https://mermaid.js.org/) (v11)** — Renderização dos diagramas de branches e commits (`gitGraph`).

## Estrutura do Projeto

```text
.
├── index.html   # Página única contendo estilos, conteúdo e diagramas
└── README.md    # Documentação do projeto
```

