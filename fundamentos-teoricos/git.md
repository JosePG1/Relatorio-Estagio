# Git

![](<../.gitbook/assets/Screenshot 2022-05-16 at 10.10.37.png>)

Git é sistema de controlo de versões, onde permite que um conjunto de developers trabalhem em conjunto com maior segurança e fluxo de trabalho, porque é possível controlar todo o histórico de alterações, e caso seja necessário revertê-las.&#x20;

A única desvantagem do Git, seria a sua complexidade ao início, em relação a todos os conteúdos associados, como:&#x20;

#### Repositórios&#x20;

É um diretório onde se armazena os arquivos de um projeto, que pode ser um repositório local, como por exemplo o computador, ou num repositório remoto, como o GitHub, BitBucket ou GitLab.   &#x20;

#### Branches&#x20;

![](../.gitbook/assets/branch.png)

Branch significa "ramo", ou seja, uma ramificação do código. Isto tem como objetivo evitar que novas funcionalidades sejam criadas sobre um determinado projeto já funcional.&#x20;

Por exemplo uma aplicação que já se encontre lancada na loja, e é necessário implementar uma nova funcionalidade, criamos um novo ramo para a desenvolver, e apos esta estar completamente funcional, efetuamos **** merge do branch no projeto original.&#x20;

Isto permito que sejam desenvolvidas diversas funcionalidades simultaneamente sem interferir com o projeto original.

#### Merge

Merge é a operação que permite pegar nos ramos independentes que foram criados, e integra-los num só ramo.

#### Commits

Um commit é conjunto de alterações que forma feitas num projeto, com uma mensagem que resume essa alteração.

Uma boa pratica ao usar o git, é a criação de commits curtos, isso pode evitar perder grandes quantidades de código, como também facilita voltar atras no código caso seja necessário.



