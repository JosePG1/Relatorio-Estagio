# Descriçāo do Trabalho

## Criaçāo de um novo ambiente de trabalho no macOS

Comecei a trabalhar num utilizar pré-existente, isto trouxe varios problemas, como por exemplo, ter acesso às credenciais de outro utilizador.

Muitos desses problemas estiveram relacionados com o Git e o SorceTree.

Para resolver isso criei um novo utilizador e configurei todas ferramentas necessárias e associei-as às minhas contas nomeadamente:

#### Chrome

Organizaçāo todas as tabs recorrentes, como por exemplo o ClickUp;

#### Slack

Login na conta

#### UnityHub

Instalaçāo da versāo correta para o projeto

Login e abertura do projeto

#### SourceTree

Login com a conta do GitHub, utilizando a respetiva chave SHH da conta

Abertura do repositório TunnyStones que já se encontra no SSD

Instalação do “homebrew” a partir do terminal

Instalação do “git-lfs” a partir do terminal do SorceTree

Git-lfs pull

Verificaçāo do estado do repositório através da linha de comandos para verificar se não                existem  comits pendentes($git status)

#### Rider

Activaçāo da licença do Rider a partir das credencias já existentes

Abertura do projeto TunnyStones

Para aceder ao repositório do projeto, também foi necessário dar permissões no SSD ao novo utilizador.



## Criaçāo e Configuracao da SSH key

Para ser possivel a criaçāo de pull requests para o repositório do projeto, foi necessáio configurar o SourceTree com a conta pessoal do GitHub e respetiva SSH key, e para isso foi necessário gerar uma seguindo os proximos passos.

### Abrir o terminal e introduzir os seguintes comandos&#x20;

#### Para criar a SSH key

```shell
$ ssh-keygen -t ed25519 -C "your_email@example.com"
```

&#x20; Se estivermos a usar um sistema antigo que nao suporta o algoritmo Ed25519

```shell
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

#### Adicionar a SSH key ao ssh-agent

```shell
$ eval "$(ssh-agent -s)"
```

### Configurar a minha conta do GitHub com a SSH key

Nas configuracões do github, foi necessário adicionar a nova SSH key gerada, e para isso bastou:&#x20;

* No Finder <img src="https://help.apple.com/assets/61D4C1B5425F2576373C512A/61D4C1B7425F2576373C5132/pt_PT/058e4af8e726290f491044219d2eee73.png" alt="" data-size="line">, selecionar Go > Go to Folder > Macintosh HD, abrir o user no qual a sessāo está iniciada, visualizar os ficheiros ocultos (Cmd+ Shift + <img src="../.gitbook/assets/computer_key_Greater_than_Period.png" alt="" data-size="line">) , e obter a SHH key publica .

#### Introduzir no terminal&#x20;

```shell
$ ssh-add "private SSH key"
```

## Criaçāo da wind animation e hook up da mesma no projeto

### Criaçāo da wind animation

#### Ajuste dos frames do sprite, para a criaçāo da animaçāo

Existem três tipos de metodos para dividir as sprite:

* Automatico: Onde nem sempre o programa faz a divisāo correta,  pois devem assumir todas a mesma medida, para nāo causar uma má animaçāo;
* Grelha por tamanho da célula: Permite ao programador ajustar da melhor maneira, seja o padding entre os frames e o tamanho da celula.
* Grelha por contagem de células: No caso em que a sprite estivesse devidamente distribuida, esta opçāo faria logo a divisāo entre o numero de colunas e linhas existentes na sprite.

Utilizamos a segunda opçāo por se tornar a opçāo mais prática neste caso.

![ Sprite de exemplo utilizada no projeto em questāo](<../.gitbook/assets/Screenshot 2022-05-12 at 11.19.57.png>)

#### Configuraçāo e implementaçāo da animaçāo  no projeto

Para a criaçāo da animaçāo, basta arranstar para a Scene a sprite.

Após criada a animaçāo, é necessário associá-la a um gameobject com um SpriteRender e um Animator.

No Sprite Render associamos a nossa sprite, e no animator a nossa animaçāo.

![Criaçāo de um objeto para implementar implementar a animaçāo](../.gitbook/assets/AnimatonImpl.png)

## Buil do projeto

Após realizaçāo de uma nova feature, ou mesmo fix de um Bug, é sempre necessário criar uma nova build do project para dar seguimento à fase de testes.

Existem várias plataformas no qual o nosso projeto pode ser lançado, como por exemplo Android, iOS, PC, ect..

![Várias plataformas para Build](<../.gitbook/assets/Screenshot 2022-05-16 at 17.10.22.png>)

### iOS

Para criar uma build para iOS, o primeiro passo será selecionar a plataforma que queremos (iOS) e trocar de plataforma nas definições da build.

![Seleçāo da plataforma para Build](<../.gitbook/assets/Screenshot 2022-05-16 at 17.12.43.png>)

Quando o Unity terminar de trocar de plataforma, no momento de fazer a build, o local onde essa build será guardada requer alguma atençāo.

Deve ser devidamente identifico, para nāo criar repetidas builds da mesma feature/bug que estamos a trabalhar.

Para conseguir testar o nosso projeto, abrimos um ficheiro com extençāo ".xcworkspace", que irá abrir o Xcode.

![Ficheiro com extençāo ".xcworkspace"](<../.gitbook/assets/Screenshot 2022-05-16 at 17.25.56.png>)

Para testar o nosso projeto, podemos fazer a build diretamente num iPad/iPhone, ou criar uma versāo teste (Archive).&#x20;

![Build da versāo teste (Archive)](../.gitbook/assets/Screenshot\_2022-05-17\_at\_14\_23\_07.png)

Esta versāo pode ser testada a partir do testfly, um serviço online para teste de aplicações, por um grupo reservado de pessoas definido pela equipa.

Em alguns casos especificos, podem surgir erros na build, sendo facilmente resolvidos com uma simples açāo.

![Resoluçāo de possiveis erros na build](../.gitbook/assets/Screenshot\_2022-05-17\_at\_14\_31\_18.png)







