# Utilidades

Comandos e informações úteis

## Cores
- 🟢 Verde (OK, sucesso, ativo)
- 🔴 Vermelho (erro, falha, crítico)
- 🟡 Amarelo (atenção, aviso, pendente)
- 🟠 Laranja (alerta intermediário)
- 🔵 Azul (informação, neutro)

## Símbolos para resultados e tarefas:
- ✅ Sucesso/concluído
- ❌ Erro/falha
- ⚠️ Atenção/alerta
- ℹ️ Informação
- 📝 Nota ou anotação
- 📌 Foco/destaque
- 🚧 Em construção
- ⏳ Em andamento
- 🔒 Protegido/privado
- 🕒 Agendado/tempo
- 🚀 Deploy, lançamento

## Outros usos comuns:
- 📁 Pasta, arquivos
- 📄 Documento
- 🗂️ Organização de tópicos
- 🛑 Parada/crítico
- 🧪 Teste
- 👀 Observação
- 💡 Dica
- 📢 Aviso
- 🛠️ Configuração/manutenção
- 🖊️ Editar
- 🏷️ Tag

## Gitlab: Clonando, Corrigindo e Subindo uma Branch de Correção

## 1. Clonando o repositório do GitLab

Primeiro, obtenha a URL do repositório (exemplo: `https://gitlab.com/usuario/nome-do-repo.git`) e use:

```sh
git clone https://gitlab.com/usuario/nome-do-repo.git
cd nome-do-repositorio
```

## 2. Criando uma branch para corrigir uma falha

É uma boa prática criar uma branch específica para cada correção ou implementação.

### Nomenclatura recomendada para branches de correção:
- `fix/nome_correcao` -> para correções de bugs comuns
- `bugfix/nome_correcao` -> para correções de bugs documentados em issues
- `hotfix/nome_correcao` -> para correções urgentes, geralmente em produção
