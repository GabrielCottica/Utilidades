## Comandos Essenciais do Linux

Referência rápida dos principais comandos para navegação, manipulação de arquivos e administração básica no terminal Linux.

---

### Navegação e Informações do Sistema

- `pwd` — Mostra o diretório atual
- `ls` — Lista arquivos e pastas
- `ls -l` — Lista detalhada (com permissões)
- `cd nome_da_pasta` — Entra em uma pasta
- `cd ..` — Volta uma pasta
- `cd ~` — Vai para a pasta pessoal (home)

---

### Manipulação de Arquivos e Pastas

- `touch arquivo.txt` — Cria arquivo vazio
- `mkdir nova_pasta` — Cria nova pasta
- `cp origem destino` — Copia arquivo/pasta
- `mv origem destino` — Move ou renomeia arquivo/pasta
- `rm arquivo.txt` — Remove arquivo
- `rm -r pasta` — Remove pasta e todo o conteúdo

---

### Visualização e Edição de Arquivos

- `cat arquivo.txt` — Exibe conteúdo do arquivo
- `less arquivo.txt` — Visualiza arquivo página a página
- `head arquivo.txt` — Mostra primeiras linhas
- `tail arquivo.txt` — Mostra últimas linhas
- `nano arquivo.txt` — Edita arquivo com nano
- `vim arquivo.txt` — Edita arquivo com vim

---

### Permissões e Proprietário

- `chmod +x arquivo.sh` — Torna arquivo executável
- `chmod 755 arquivo` — Permissões de leitura, escrita e execução para dono (7), leitura e execução para grupo e outros (5 e 5)
- `chmod 644 arquivo` — Leitura e escrita para dono (6), leitura para grupo e outros (4 e 4)
- `chmod 700 arquivo` — Todas as permissões para dono, nenhuma para grupo e outros
- `chmod 600 arquivo` — Leitura e escrita para dono, nenhuma para grupo e outros
- `chmod 777 arquivo` — Todas as permissões para todos (dono, grupo e outros)
- `chown usuario:grupo arquivo` — Altera dono e grupo do arquivo

**O que significam as permissões?**

Cada dígito representa permissões para: **dono** / **grupo** / **outros**.
- **r (read)**: Leitura do arquivo
- **w (write)**: Escrita (modificação)
- **x (execute)**: Execução (rodar como programa/script)

Exemplo: `chmod 754 arquivo`
- **7 (rwx)** — dono: leitura, escrita e execução
- **5 (r-x)** — grupo: leitura e execução
- **4 (r--)** — outros: apenas leitura

Para ver as permissões atuais de arquivos/pastas:
- `ls -l`

---

### Sistema e Processos

- `top` — Monitora processos em tempo real
- `ps aux` — Lista todos os processos
- `kill PID` — Encerra processo pelo PID
- `df -h` — Mostra uso de espaço em disco
- `du -sh pasta` — Mostra tamanho da pasta
- `free -h` — Exibe uso de memória RAM

---

### Rede

- `ping google.com` — Testa conexão com host
- `ifconfig` ou `ip a` — Mostra configurações de rede
- `curl site.com` — Faz requisição HTTP simples
- `wget url` — Baixa arquivos da internet

---

### Busca de Arquivos

- `find /caminho -name "nome_do_arquivo"` — Busca arquivos por nome a partir de um diretório
- `find . -type f -name "*.txt"` — Busca todos os arquivos `.txt` na pasta atual e subpastas
- `locate nome_do_arquivo` — Busca rápida por arquivos (base de dados pré-indexada, pode exigir `sudo updatedb` para atualizar)
- `grep "palavra" arquivo.txt` — Busca palavra em um arquivo
- `grep -r "palavra" pasta/` — Busca palavra em todos os arquivos da pasta (recursivo)
- `grep -i "palavra" arquivo.txt` — Busca ignorando maiúsculas/minúsculas

**Exemplo de uso do find:**

```sh
find /home/usuario/Documentos -type f -name "*.pdf"
```
_Busca todos os arquivos PDF dentro de /home/usuario/Documentos e suas subpastas._

**Outros exemplos:**

* Buscar arquivos modificados nas últimas 24 horas:
```sh
find . -type f -mtime -1
```

* Buscar arquivos com permissão exata 777:
```sh
find /var/www -type f -perm 0777
```
_Lista arquivos com permissão total (leitura, escrita e execução para todos) dentro de /var/www._

**O que significa cada opção?**

`-type f`: limita a busca a arquivos comuns (ignora diretórios, links, etc.)

`-name "padrão"`: busca arquivos pelo nome, podendo usar curingas (ex: `*.txt`)

`-mtime -1`: arquivos modificados há menos de 1 dia (`-2` = menos de 2 dias, `1` = exatos 1 dia atrás)

`-perm 0777:` busca arquivos com permissão exata 777 (todos podem ler, escrever e executar)

Exemplo:
```sh
find . -type f -name "*.txt"
```
Procura, a partir do diretório atual (`.`), todos os arquivos (não pastas) terminados em `.txt`.

### Dicas Rápidas

* Completar comandos/nomes de arquivos: `Tab`

* Histórico de comandos: Use as setas ↑ e ↓

* Executar último comando: `!!`

* Comando anterior com sudo: `sudo !!`