
# Git

Git é sistema de controlo de versões, que permite que vários developers trabalharem em conjunto com maior segurança e fluxo de trabalho, porque é possível navegar todo o histórico de alterações, e caso seja necessário revertê-las.&#x20;

&#x20;Existem outras tecnologias para além do Git. Estas podem ser classificadas em duas grandes categorias:

### Sistemas de versionamento centralizados

* CVS, SVN e Perforce (standard na industria dos videijogos) possuem um repositório central, onde os developers fazem checkouts e commits.

### Sistemas de versionamento distribuidos&#x20;

* É o caso do Git, Mercurial e Bazaar, onde não existe um repositório central.

Os membros da CPDS usam Git para todos so projetos.

Outra grande razão para o uso do Git, é a enorme variedade de comandos, como git clone que permite clonar um projeto, ou git status para saber o estado do repositório, e o quão bem documentado está.   &#x20;

Para trabalhar com git e source control é necessário compreender alguns conceitos:&#x20;

### Repositórios&#x20;

É um diretório onde se armazena os arquivos de um projeto, que pode ser um repositório local, como por exemplo o computador, ou num repositório remoto, como o GitHub, BitBucket ou GitLab.   &#x20;

### Branches&#x20;



![](.gitbook/assets/branch.png)

Branch significa "ramo", ou seja, uma ramificação do código. A utilização de branches tem como objetivo evitar que novas funcionalidades sejam criadas sobre um determinado projeto já funcional.&#x20;

Quando pretendemos adicionar uma nova feature a uma app já em loja, o desenvolviemnto de essa feature nunca vai ser feita sobre o projeto original.

Para isso criamos um branch, relativamente ao branch principal do projeto ('main trunk', normalmente chamado de 'master'), para assim desenvolver essa nova feature sem causar conflitos com o original.

Após testada a nova feature, e concluido que está pronta para ser lançada, avançamos com merge no "master",  para que assim faça parte da aplicação.

Isto permito que sejam desenvolvidas diversas funcionalidades simultaneamente sem interferir com o projeto original.

### Merge

Merge é a operação que permite juntar ramos independentes num só.

### Commits

Um commit é conjunto de alterações com uma mensagem que as resume.

Uma boa prática ao usar o git, é a criação de commits curtos. Usar commist granulares pode evitar perder grandes quantidades de código, e facilita reverter código quando necessário.



### Git LFS

Quando efetuamos clone de um repositório, é feito o download de todo o seu histórico.

Clonar projetos com grandes ficheiros, como por exmplo audio ou vídeo é um processo muito demorado e que pode ocupar muito espaço em disco.

Git LFS é uma extençāo Git, que reduz o impacto desses ficheiros no repositório, sendo transferidos só quando necessário.

Resumidamente, grande ficheiros são transferidos no processo de checkout e não durante a clonagem.&#x20;

O Git é o padrão do mercado hoje para versionamento de código, essencial para qualquer programador, independentemente das linguagens dos projetos, assim sendo essencial familiarizar-se com este sistema.
