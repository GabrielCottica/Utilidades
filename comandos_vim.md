## Comandos Essenciais do VIM/VI

Referência rápida dos principais comandos do editor VIM/VI.

---

### Modos de Operação

- **Normal:** Navegue e edite (pressione `Esc` para acessar)
- **Inserção:** Digite texto (`i`, `I`, `a`, `A`, `o`, `O`)
- **Visual:** Selecione texto (`v`, `V`, `Ctrl+v`)
- **Linha de Comando:** Execute comandos (`:`)

---

### Navegação

- `h` `j` `k` `l` – Esquerda, baixo, cima, direita
- `0` / `$` – Início / fim da linha
- `w` / `b` – Próxima / palavra anterior
- `gg` / `G` – Início / fim do arquivo
- `Ctrl+f` / `Ctrl+b` – Avança / volta uma página

---

### Inserção de Texto

- `i` – Insere antes do cursor
- `I` – Insere no início da linha
- `a` – Insere após o cursor
- `A` – Insere no final da linha
- `o` – Nova linha abaixo
- `O` – Nova linha acima

---

### Edição

- `x` – Apaga caractere sob o cursor
- `dd` – Remove (corta) linha
- `yy` – Copia linha
- `p` – Cola abaixo do cursor
- `u` – Desfaz última ação
- `Ctrl+r` – Refaz ação desfeita
- `r` – Substitui caractere sob o cursor

---

### Busca e Substituição

- `/palavra` – Busca para frente
- `?palavra` – Busca para trás
- `n` / `N` – Próxima / anterior ocorrência
- `:%s/antigo/novo/g` – Substitui todas as ocorrências

---

### Seleção Visual

- `v` – Seleção por caractere
- `V` – Seleção por linha
- `Ctrl+v` – Seleção em bloco (coluna)

---

### Salvar e Sair

- `:w` – Salva
- `:q` – Sai
- `:wq` – Salva e sai
- `:q!` – Sai sem salvar

---

### Dicas Rápidas

- Mostrar linhas numeradas: `:set number`
- Abrir arquivo: `vim nome_arquivo`
- Para sair do modo inserção, pressione `Esc`

---