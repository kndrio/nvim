```bash
git clone https://github.com/owhska/nvim-work.git && mv nvim ~/.config/nvim
```
# Keybinds do Neovim (init.lua – Linux)

- **Leader:** `<Space>` (`vim.g.mapleader = " "`)
- **timeoutlen:** 300 ms (o `which-key` aparece após 300 ms)
- Legenda de modos: **n** = normal, **v** = visual, **x** = visual (seleção), **o** = operator-pending, **i** = insert

---

## 1. Arquivo, janelas e abas

| Atalho | Modo | O que faz |
|---|---|---|
| `<leader>ww` | n | Salvar arquivo (`:write`) |
| `<leader>wq` | n | Sair da janela (`:quit`) |
| `<leader>e` | n | Abrir explorador netrw (`:Ex`) |
| `<leader>n` | n | Novo arquivo (`:enew`) |
| `<leader>q` | n | Fechar aba (`:tabclose`) |
| `<leader>wv` | n | Split vertical |
| `<leader>ws` | n | Split horizontal |
| `<leader>wh` | n | Ir para janela à esquerda |
| `<leader>wj` | n | Ir para janela abaixo |
| `<leader>wk` | n | Ir para janela acima |
| `<leader>wl` | n | Ir para janela à direita |
| `sv` | n | Split vertical |
| `ss` | n | Split horizontal |
| `sx` | n | Fechar janela atual |
| `<leader><Tab>` | n | Próxima aba |
| `<leader><S-Tab>` | n | Aba anterior |
| `<leader>N` | n | Nova aba (`:tabnew`) |
| `<leader><Left>` | n | Aumentar largura da janela (+20) |
| `<leader><Right>` | n | Diminuir largura da janela (−20) |
| `<leader><Up>` | n | Aumentar altura da janela (+10) |
| `<leader><Down>` | n | Diminuir altura da janela (−10) |
| `<leader>X` | n | `chmod +x` no arquivo atual |
| `<leader>lw` | n | Alternar quebra de linha (`wrap`) |

## 2. Buffers

| Atalho | Modo | O que faz |
|---|---|---|
| `<leader>bd` | n | Deletar buffer (`:bdelete!`) |
| `<leader>bn` | n | Novo buffer vazio (`:enew`) |

## 3. Navegação e edição

| Atalho | Modo | O que faz |
|---|---|---|
| `<S-h>` | n, o, x | Ir para o início da linha (`^`) |
| `<S-l>` | n, o, x | Ir para o fim da linha (`g_`) |
| `<C-u>` | n | Meia página para cima, centralizando (`zz`) |
| `<C-d>` | n | Meia página para baixo, centralizando (`zz`) |
| `n` | n | Próxima ocorrência da busca, centralizada |
| `N` | n | Ocorrência anterior da busca, centralizada |
| `<C-a>` | n | Selecionar o arquivo inteiro (`gg<S-v>G`) |
| `<` | v | Indentar para a esquerda mantendo a seleção |
| `>` | v | Indentar para a direita mantendo a seleção |
| `K` | v | Mover linhas selecionadas para cima |
| `J` | v | Mover linhas selecionadas para baixo |
| `x` | n | Apagar caractere **sem** copiar para o registrador |
| `<leader>dd` | n, v | Apagar **sem** copiar para o registrador (`"_d`) |
| `p` | x | Colar sobre a seleção **sem** perder o conteúdo copiado |
| `<leader>rr` | n | Substituir a palavra sob o cursor no arquivo todo (abre `:%s` já preenchido) |
| `<leader>m` | v | Comentar/descomentar as linhas selecionadas |
| `<leader>cf` | n | Copiar o nome/caminho do arquivo para o clipboard |

## 4. Busca e fuzzy finder (fzf-lua)

| Atalho | Modo | O que faz |
|---|---|---|
| `<leader>f` | n | Buscar arquivos |
| `<C-p>` | n | Buscar arquivos versionados pelo git |
| `<leader><leader>` | n | Live grep no projeto |
| `<leader>s` | n | Busca fuzzy nas linhas do buffer atual |
| `<leader>gg` | n | Live grep somente em arquivos do git (`git grep`) |
| `<leader>ch` | n | Buscar nas help tags |
| `<leader>ck` | n | Buscar keymaps |
| `<leader>cs` | n | Menu de pickers do fzf-lua (`builtin`) |
| `<leader>cw` | n | Grep da palavra sob o cursor |
| `<leader>cd` | n | Diagnósticos do documento |
| `<leader>cD` | n | Diagnósticos do workspace |
| `<C-x>` | n | Seletor de diretórios – muda o diretório da janela atual |
| `<leader>x` | n | Seletor de diretórios – abre em nova aba (`tcd`) |
| `<leader>/` | n | Pesquisa web (DuckDuckGo) em janela flutuante |

### Dentro da janela de pesquisa web

| Atalho | O que faz |
|---|---|
| `q` | Fechar a janela |
| `<Esc>` | Fechar a janela |
| `<CR>` | Abrir o link da linha atual no navegador (`xdg-open`) |

## 5. Git

| Atalho | Modo | O que faz |
|---|---|---|
| `<leader>gt` | n | Fugitive – `:Git` (status) |
| `<leader>gc` | n | `:Git commit` |
| `<leader>gl` | n | Log de commits (fzf-lua) |
| `<leader>gs` | n | Git status (fzf-lua) |
| `<leader>gd` | n | Branches (fzf-lua) |
| `<leader>gb` | n | Histórico do arquivo atual (fzf-lua) |
| `<leader>gg` | n | Git grep (fzf-lua) |
| `<leader>d` | n | Abrir Diffview |

## 6. LSP e diagnósticos

| Atalho | Modo | O que faz |
|---|---|---|
| `gd` | n | Ir para a definição |
| `K` | n | Hover (documentação) |
| `<leader>vww` | n | Buscar símbolo no workspace |
| `<leader>vd` | n | Abrir float de diagnóstico |
| `<leader>vca` | n | Code action |
| `<leader>vrr` | n | Referências |
| `<leader>vrn` | n | Renomear símbolo |
| `<C-h>` | i | Signature help |
| `[d` | n | Próximo diagnóstico (`goto_next`) |
| `]d` | n | Diagnóstico anterior (`goto_prev`) |
| `]e` | n | Próximo item da quickfix (centraliza) |
| `[e` | n | Item anterior da quickfix (centraliza) |
| `<leader>co` | n | Abrir quickfix |
| `<leader>T` | n | Trouble: diagnósticos |
| `<leader>lT` | n | Trouble: quickfix |

## 7. Testes (neotest)

| Atalho | Modo | O que faz |
|---|---|---|
| `<leader>vtn` | n | Rodar o teste mais próximo |
| `<leader>vtf` | n | Rodar todos os testes do arquivo |
| `<leader>vts` | n | Alternar painel de resumo |
| `<leader>vto` | n | Abrir output do teste (e entrar nele) |

## 8. Harpoon

| Atalho | Modo | O que faz |
|---|---|---|
| `<leader>a` | n | Adicionar arquivo atual ao Harpoon |
| `<C-e>` | n | Abrir/fechar menu rápido do Harpoon |
| `<leader>1` | n | Ir para o arquivo 1 |
| `<leader>2` | n | Ir para o arquivo 2 |
| `<leader>3` | n | Ir para o arquivo 3 |
| `<leader>4` | n | Ir para o arquivo 4 |

## 9. Ferramentas, plugins e terminal

| Atalho | Modo | O que faz |
|---|---|---|
| `<leader>t` | n | Terminal `zsh` num split inferior (12 linhas) |
| `<leader>i` | n | Abrir `agy` num vsplit (largura 50) |
| `<leader>o` | n | Abrir `opencode` (modelo `litellm-pr/gemma4-saj`) num vsplit |
| `<leader>b` | n | Alternar NvimTree |
| `<leader>u` | n | Alternar Undotree |
| `<leader>z` | n | Zen Mode |
| `<leader>cp` | n | Abrir color picker (oklch) |
| `<leader>cP` | n | Color picker na cor sob o cursor |
| `<leader>ll` | n | Status do Packer (`:PackerStatus`) |
| `<leader>lm` | n | Abrir o Mason |

## 10. Múltiplos cursores (vim-visual-multi)

| Atalho | Modo | O que faz |
|---|---|---|
| `;s` | n | Selecionar a palavra sob o cursor (find under) |
| `;n` | n | Adicionar cursor na próxima ocorrência |
| `;a` | n | Selecionar todas as ocorrências |

## 11. Autocompletar (blink.cmp)

Preset `default` do blink.cmp + as seguintes customizações:

| Atalho | Modo | O que faz |
|---|---|---|
| `<C-Space>` | i | Mostrar menu / alternar documentação |
| `<Tab>` | i | Próximo item / avançar snippet |
| `<S-Tab>` | i | Item anterior / voltar snippet |
| `<C-n>` | i | Próximo item |
| `<C-p>` | i | Item anterior |
| `<C-y>` | i | Aceitar item |
| `<C-e>` | i | Esconder o menu |

## 12. Autopairs (customizado)

No modo **insert**, ao digitar o caractere de abertura o par é inserido automaticamente; se o próximo caractere já for o fechamento, o cursor apenas pula por cima dele.

| Digitado | Resultado |
|---|---|
| `(` | `()` |
| `[` | `[]` |
| `{` | `{}` |
| `"` | `""` |
| `'` | `''` |
| `` ` `` | ` `` ` |

## 13. Dashboard (tela inicial, sem argumentos)

Atalhos válidos apenas no buffer do dashboard:

| Atalho | O que faz |
|---|---|
| `n` | Novo arquivo |
| `f` | Buscar arquivo (fzf-lua) |
| `e` | Explorador de arquivos (`:Ex`) |
| `wq` | Sair (`:q!`) |

---

## Observações sobre a config

1. **`[d` / `]d` estão invertidos** em relação ao padrão do Neovim: `[d` chama `goto_next` e `]d` chama `goto_prev`. Se não for intencional, basta trocar.
2. **`<leader>vr` no which-key** está descrito como "LSP references", mas o atalho real é `<leader>vrr`.
3. **Prefixos que compartilham teclas** (`<leader>d` × `<leader>dd`, `<leader>b` × `<leader>bd`/`<leader>bn`, `<leader>w` × `<leader>ww`/`wq`/...): como o `timeoutlen` é 300 ms, os atalhos curtos só disparam depois desse tempo de espera.
4. **`<Tab>` e `<C-i>`** são a mesma tecla em muitos terminais, então o remap de `<Tab>` para `:bnext` sobrescreve o `<C-i>` (avançar no jumplist).
5. **`<C-e>`** tem dois usos diferentes: Harpoon no modo normal e "esconder menu" do blink.cmp no modo insert (sem conflito, pois os modos são distintos).
6. **`<C-p>`** também tem usos diferentes: git files no modo normal e "item anterior" no autocomplete (modo insert).
7. **Autopair de `'`** insere par mesmo em contextos como apóstrofos em texto (ex.: `don't`), o que pode atrapalhar em arquivos de texto/markdown.
