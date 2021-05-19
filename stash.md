# Stash

### git stash

O git stash é uma forma de "varrer" o código que ainda não está pronto para baixo do tapete, para que possamos trabalhar em outra branch e fazer outras funcionalidades.

Ele é uma alternativa para salvar códigos incompletos ou que não foram finalizados, sem a necessidade de fazer um commit.

    git stash

Tudo que não foi consolidado em um commit será "escondido".

#### git stash list

Listar o que ja foi escondido:

    git stash list


#### git stash show

Traz informações do que está salvo no topo da pilha.

    git stash show

#### git stash save

Esconde as alterações e adiciona uma mensagem de referência.

    git stash save "Nome da alteração."

#### git stash apply

Faz uma busca pelo indice do que foi escondido, copia e mantem o conteúdo na pilha do stash.

    git stash apply 1 

O número 1 é referente ao indice no exemplo.

#### git stash pop

Desempilha o priemiro item do stash, removendo o conteúdo e jogando no branch paras ser commitado.

    git stash pop

#### git stash drop

É utilizado para apagar algum item do stash.

    git stash drop 0

O número 0 é referente ao índice.

#### git stash clear

Apaga toda a pilha do que foi escondido no stash.

    git stash clear