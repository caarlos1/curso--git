# git flow

O git flow é um fluxo de trabalho que visa ditar regras de relacionamentos entre branchs, megres, padrões de nomeclatura e outros detalhes.

## github flow

É um fluxo simplificado que sugere que exista uma branch master e seja criado branches de feature e bugfix, quando necessário.

Esse fluxo de trabalho é bastante simples e visa apenas proteger a integridade da branch master.

É uma opção para aplicações pequenas e com poucos desenvolvedores.

## git flow

Um conjunto de extensões para o git que provê operações de alto nível para repositórios usando o modelo de branches de Vicent Driessen.

### git flow init

Par iniciar um repositório com git flow é bem parecido com o o git normal:

    git flow init

Serão feitas perguntas sobre os nomes das branchs e pronto.

### features

#### Criando uma feature:

    git flow feature start nome_feature

Por padrão será adicionado o "feature/".

#### Encerrando uma feature:

    git flow feature finish nome_feature

Ao executar essa função, automaticamente será feito um merge com a branch develop e a branch de feature será removida.

### release

#### Criando uma release:

    git flow release start 0.1.0

Por padrão será adicionado o "release/".

#### Encerrando uma release:

    git flow release finish 0.1.0

Ao finalizar uma release, será feito um merge com a master e a develop, adicionando uma mensagem de merge e tag. Além de excluir o branch de release.

### hotfix

O hotfix usa a mesma lógica do release de criação e finalização, porem, será feito um merge com a master e develop.

