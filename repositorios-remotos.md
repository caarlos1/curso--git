# Repositórios Remotos

### Principais:

- GitLab - Mais utilziados por empresas.
- GitHub - Códigos open source e também empresarial.
- Bitbucket - Serviço da Atlassian

## Comandos:

### git remote

Adicionando repositório remoto:

    git remote add origin https://github.com/caarlos1/git-curso.git

O "origin" é o nome que damos para o repositório remoto. Em seguida adicionamos o link do repositório.

#### Removendo:

    git remote remove origin

#### Listando repositórios remotos:

    git remote

#### Listando informações:

    git remote show github

### git push

Para subir a branch principal para o repositorio remoto usamos o push:

    git push github master

Para subir todas as branch:

    git push github --all

#### Definindo comando automatico de push:

    git push -u github --all

Dessa forma, quando digitarmos git push, será executado o push no "github --all"

### git push ... --force

Caso tenha que dar push em um diretório remoto de um projeto que tive que remover alguns commits, o diretório remoto não aceitara e acusará mensagens.

Para resonver isso, é necessarios forçar que o diretório remoto seja atualizado com o --force:

    git push github --force

Porém, isso funcionará **apenas para branchs secundarias,** a nossa branch master será protegida e não aceitará o "--force" por padrão.

### git pull

O git pull atualiza meu repositório com o remoto e mescla os commits.

    git pull

### git fetch

O git fetch tem a mesma função que o git pull, porem não adiciona os commits automaticamente, tendo a necidade de fazer um merge depois de feito.

    git fetch

A vantagem principal é a opção de verificar o que foi modificado, antes de inserir no nosso repositório local.

Para visualiziar o fetch será necessário fazer um checkout:

    git checkout github/master

Sendo que o **github** é o nome do seu repositório remoto e **master** a branch que fez o fetch.

### git clone

Para clonar um repositório, é muito simples:

    git clone https://github.com/caarlos1/git-curso.git

O repositório será clonado na pasta atual.

### git reflog

Para ver o histórico geral das ações feitas no repositório git:

    git reflog

### git cherry-pick

Para recuperar repositórios apagados ou desfazer alguma modificação :

    git cherry-pick hash_versao_do_repo

Para descobrir o hash, utilize o **git reflog.**

## Probelmas Comuns:

https://stackoverflow.com/questions/15589682/ssh-connect-to-host-github-com-port-22-connection-timed-out
