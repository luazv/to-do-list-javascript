# 📝 Daily List

Uma lista de tarefas (to-do list) simples, feita em **HTML, CSS e JavaScript puro**, com suporte a **tema claro e escuro** e armazenamento local das tarefas no navegador.

🔗 **Acesse online:** [luazv.github.io/to-do-list-javascript](https://luazv.github.io/to-do-list-javascript)

---

## Funcionalidades

- Adicionar novas tarefas
- Adicionar tarefas pressionando **Enter** (sem precisar clicar no botão)
- Marcar/remover tarefas concluídas
- Validação para não permitir tarefas vazias ou duplicadas
- Alternância entre **tema claro** e **tema escuro**
- Tarefas salvas automaticamente no `localStorage` do navegador
- Tema salvo entre sessões (o navegador lembra da última escolha)
- Layout simples e responsivo

---

## Estrutura do projeto

```
to-do-list-javascript/
├── index.html          # Estrutura da página
├── style.css           # Estilos e variáveis de tema (claro/escuro)
├── script.js            # Lógica da lista de tarefas e do tema
├── assets/
│   └── fonts/
│       └── fonts.css   # Fonte customizada usada no projeto
└── README.md
```

---

## Como usar

### Online
Basta acessar o link publicado via GitHub Pages (veja acima). Funciona em qualquer navegador, computador ou celular.

### Localmente
1. Clone o repositório:
   ```bash
   git clone https://github.com/luazv/to-do-list-javascript.git
   ```
2. Abra o arquivo `index.html` diretamente no navegador (duplo clique) ou use uma extensão como *Live Server* no VS Code.

---

## Como funciona o tema claro/escuro

- O tema é controlado através do atributo `data-theme` na tag `<html>`, que alterna entre `"light"` e `"dark"`.
- As cores de toda a interface são definidas como **variáveis CSS** (`--bg-color`, `--text-color`, etc.), que mudam automaticamente conforme o tema ativo.
- Ao clicar no botão de tema (ícone de sol ☀️ ou lua 🌙), o tema é trocado e salvo no `localStorage`, para que a preferência seja lembrada na próxima visita.
- Se o usuário nunca escolheu um tema manualmente, o site detecta automaticamente a preferência do sistema operacional (`prefers-color-scheme`).
- Um pequeno script no `<head>` aplica o tema **antes** da página renderizar, evitando o efeito de "flash" de tela clara ao carregar em modo escuro.

---

## Armazenamento dos dados

As tarefas são salvas no **`localStorage`** do navegador, sob a chave `to-do-list-gn`. Isso significa que:

- As tarefas ficam salvas mesmo se você fechar e reabrir o navegador.
- Cada navegador/aparelho possui sua **própria lista independente** — não há sincronização entre dispositivos diferentes.
- Não é necessário nenhum backend, banco de dados ou login para usar o app.

---

## Tecnologias utilizadas

- **HTML5**
- **CSS3** (variáveis CSS para temas)
- **JavaScript** (vanilla, sem frameworks ou bibliotecas)
- **localStorage** (Web Storage API)

---

## Autor

Projeto desenvolvido por [luazv](https://github.com/luazv).