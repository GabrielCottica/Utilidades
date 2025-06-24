## Gitlab: Clonando, Corrigindo e Subindo uma Branch de Correção

### 1. Clonando o repositório do GitLab
Primeiro, obtenha a URL do repositório (exemplo: `https://gitlab.com/usuario/nome-do-repo.git`) e use:

```sh
git clone https://gitlab.com/usuario/nome-do-repo.git
cd nome-do-repositorio
```

### 2. Criando uma branch para corrigir uma falha
É uma boa prática criar uma branch específica para cada correção ou implementação.

#### Nomenclatura recomendada para branches de correção:
- `fix/nome_correcao` -> para correções de bugs comuns
- `bugfix/nome_correcao` -> para correções de bugs documentados em issues
- `hotfix/nome_correcao` -> para correções urgentes, geralmente em produção

No diretório do repositório, execute o comando para **criar** e alternar para uma nova branch. Use uma das nomenclaturas sugeridas conforme o contexto da correção:

```sh
# Exemplo para uma correção comum
git checkout -b fix/ajusta-leitura-arquivo

# Exemplo para um bug registrado em issue
git checkout -b bugfix/corrige-nome-usuario

# Exemplo para uma correção urgente
git checkout -b hotfix/corrige-erro-login
```

### 3. Fazendo as correções necessárias
Faça todas as alterações necessárias.

```sh
# Exemplo para abrir o arquivo utilizando o editor nano
nano arquivo_que_vai_corrigir.py
```

### 4. Adicionando e commitando as mudanças
Após concluir as alterações, adicione os arquivos modificados ao staging area e faça o commit com uma mensagem clara e objetiva:

```sh
# Exemplo adicionando arquivos modificados
git add arquivo_que_vai_corrigir.py
git commit -m "Corrige leitura de arquivo na função X"
```

Se houver múltiplos arquivos, você pode usar:
```sh
# Exemplo adicionando múltiplos arquivos modificados
git add .
git commit -m "Corrige múltiplos bugs relacionados à leitura e escrita"
```

### 5. Enviando a branch de correção para o GitLab
Agora, envie sua branch para o repositório remoto no GitLab:
```sh
# Exemplo - substitua pelo nome da sua branch.
git push origin fix/ajusta-leitura-arquivo
```

### 6. Abrindo um Merge Request (MR) no GitLab
1. Acesse o repositório no GitLab.
2. O GitLab geralmente sugere automaticamente a abertura de um Merge Request assim que identifica uma nova branch remota.
3. Clique em “Create merge request”.
4. Preencha o título e a descrição do MR, explicando claramente o que foi corrigido.
5. Selecione revisores e assignees, se necessário.
6. Clique em “Submit” para criar o MR.

### 7. Boas práticas após o Merge Request
* Aguarde revisão dos colegas ou do responsável pelo repositório.

* Faça ajustes adicionais na mesma branch, se necessário, e repita o git add, commit e push.

* Após o merge, lembre-se de atualizar sua branch principal local:

```sh
# Atualizando a branch principal local
git checkout main
git pull origin main
```

### RESUMO DO FLUXO
Clonar → Criar Branch → Corrigir → Commitar → Push → MR → Merge → Atualizar main