# Aplicando .gitignore no seu projeto

## O .gitignore quando usado em um projeto, ignora arquivos e diretórios sensíveis ou desnecessários que você não quer que sejam rastreado pelo versionamento do seu código.

# **CRIANDO E CONFIGURANDO O  .gitignore**

```bash
# no terminal PowerShel crie o arquivo .gitignore no projeto
New-Item .gitignore -ItemType File
# terminal comum:

touch .gitignore

**# dentro do arquivo .gitignore adicione o que deseja ser ignorado com suas respectivias extensões
Ex:**
node_modules/
.env

**# caso os arquivos já estiverem sendo versionados, o git continuará rastreando os arquivos, para impedir isso use no terminal:**
git rm --cached -r node_modules .env
git commit -m "Ocultando arquivos sensíveis"
git push

```

# **ADICIONANDO ARQUIVOS DE VOLTA NO GIT**

```bash
# Remova as linhas do .gitignore:
# node_modules/
# .env

# Depois:
git add node_modules .env
git commit -m "Adicionando arquivos ocultados"
git push

```

# DICA

```jsx
Use um gerador automático de **.gitignore** de acordo com a tecnologia que você está usando:

# https://www.toptal.com/developers/gitignore
```

# DOCUMENTAÇÃO

Leia a documentação oficial do Git para entender mais sobre o funcionamento do .gitignore:

https://git-scm.com/docs/gitignore/pt_BR

Links importantes
Tutorial no Notion: https://www.notion.so/Aplicando-gitignore-no-seu-projeto-23e78843b38a80148a37cfee91a67cdb
