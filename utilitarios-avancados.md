# Utilitários Avançados

### Branch

Branch é como um galho, uma ramificação do projeto principal.

#### Boas práticas:

- Não desenvolver dentro da **branch master.**
- A master ou main deve possuir apenas o código confiavel, testado e aplicado em produção. Nada além disso!

Criando branch com checkout:

    git checkout -b feature/client

Caso não exista a "feature/client" o "-b" cria uma nova branch e faz checkout dentro dela.

#### Comandos:

Para vizualizar todas as branch:

    git branch

Removendo branch:

    git branch -d nome_da_branch

### git merge:

Para fazer um merge, primeiro **faça checkout no branch principal** (que vai receber o conteúdo), e faça o seguinte comando:

    git merge nome_da_branch

Será criando um novo commit informando o merge. Caso queira desfazer o merge, use o reset para voltar 1 commit:

    git reset HEAD~1 --hard

O "--hard" removerá os arquivos para não causar confusão.

##### Organização dos commits:

A organização do **git merge** padrão juntará os commits na sequencia de tempo que os commits foram criados.

#### --squash

Busca as alterações e arquivos diferentes do branch secundário e os coloca para serem commitados no master.

    git merge feature/x --squash

Recomendável para **não poluir a branch principal.**

### git rebase:

Junta as branchs, mas ao contrario do merge que mescla os commits, o rebase insere todos os commits no lugar em que foi criado o primeiro commit do branch secundario.

    git rebase feature/x

Nesse caso, hão há um novo commit, apenas a inserção dos que ja existem dentro da branch master.

O uso na branch master não é recomendável, já que o rebase é mais difícil de ser desfeito comparado ao merge.

#### Quando usar?

O uso é recomendado quando é necessário copiar o conteúdo da branch master para alguma secundária.


### git checkout

Recuperando versão de apenas um arquivo de um commit antigo:

    git checkout hash_commit nome_do_arquivo

Depois disso será recuperada a versão do arquivo referente a hash e já adicionada na track para commitar.