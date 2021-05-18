# Comandos Git

## Básico

Inicializando git em um diretório:

    git init

Verificando situação dos arquivos:

    git status

Documentação:

    git help

### Track:

    git add arquivo.txt

#### Opções:

    // Track de forma interativa:
    git add -i

    // Track de tudo:
    git add .

### git commit

Commit simples e básico:

    git commit -m "Criação do arquivo x"

Commit utilziando editor auxiliar:

    git commit

### .gitignore

Para ignorar arquivos e diretórios é necessario criar um arquivo chamado ".gitignore" e adicionar o nome das pastas, extensões e arquivos. Ex:

    node_modules
    build
    *.out

### git diff

Mostrar alteração feitas nos arquivos commitados:

    git diff

### git log

Exibir logs dos commits feitos:

    git log

Opções:

    git log --oneline

### Remendando Commit

Para remendar um commit feito, ou seja, sobescrever com outro que tenha alguma correção ou código diferente, é necessario usar o "--amend". Ex:

    git commit -m "Mensagem do comit remendo." --amend

Fazendo isso, o último commit será subistituido pelo novo.

### git reset

Resetando commits continuando com as edições: 

    git reset HEAD~1 --soft
    
    // HEAD~1 define o número de commits para 1.

Resetando e sumindo com as edições:

    git reset HEAD~1 --hard

### git checkout

Retorna o estado do arquivo referente ao último commit:

    git checkout arquivo.txt

Descarta as alterações de todos os arquivos:

    git checkout .

### git rm

Adicionar a remoção dos arquivo no commit, similar ao add mas apenas para arquivos excluidos.

    git rm arquivo.txt

### git tag

Tags são usadas para rotular versões e conseguirmos transitar por elas de forma fácil, sem a necessidade de  utilizar a hash do header.

    git tag v1.0.0

Depois de referência-las, podemos voltar para essa versão usando por exemplo o checkout:

    git checkout v1.0.0

Pronto, voltaremos para a versão "v1.0.0".

### git show

Busca as informações de um commit que quero visualizar.

    git show 098463e

Usamos o hash, mas também é possível usar tags.