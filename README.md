# Tutorial de Git/GitHub pós Pixel Init

## Sobre:


Hoje você irá iniciar seu primeiro repositório no GitHub!

Bom, então você viu minha palestra sobre Git e ficou interessado? Legal! Aqui vou explicar de forma mais detalhada e prática como funciona essa ferramenta maravilhosa.
Como primeiro exercício vamos iniciar seu primeiro repositório(projeto)!

## Primeiro passo:

Inicialmente começaramos fazendo sua conta GitHub. É muito simples! 

Acesse: https://github.com/join

![github-join](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/github-join.png)


A primeira etapa(vista na foto) consiste apenas em preencher seus detalhes, a segunda você aceitar o plano gratuito e continuar e finalmente a terceira (opcional) é um questionário sobre suas habilidades com programação.

Após a conclusão das etapas e verificação do seu e-mail você se deparará com a seguinte tela:


![github-new](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/github-new.png)

**Aqui você iniciará seu primeiro repositório!!!!**

![github-new](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/github-new-modified.png)

*Não utilize a opção "initialize this repository with a README", o arquivo será criado logo em seguida.*


Agora que você criou seu repositório você verá a seguinte tela:

![github-first-repo](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/github-setup-repo.png)

Não se assuste, já já utilizaremos essa tela. Por enquanto, porém, deixe-a minimizada (Não feche!). 

## Segundo passo:

Bom, agora que já temos o repositório do GitHub pronto vamos a sua máquina local para fazer a instalação da ferramenta git! Utilizaremos a linha de comando (terminal/shell/prompt de comando) para fazer a instalação. O intuito é você se familiarizar, você vai utilizar bastante essa telinha no futuro!

### Instalação:

#### Ubuntu:

Primeiramente, atualize seus pacotes:

`$ sudo apt update `

Faça a instalação do git usando o comando apt-get:

`$ sudo apt-get install git`

Finalmente, verifique se o git foi instalado corretamente:

`$ git --version`

#### Windows:

Siga o link para o [instalador do Git no Windows](https://gitforwindows.org/). Utilize todas as configurações padrão.

Assim que a instalação terminar, abra o aplicativo *GitBash* e verifique se o git foi instalado corretamente:

`$ git --version`


### Configurações globais:

Quase lá, agora só precisamos fazer mais alguns ajustes. Insira os seguintes comandos no seu ambiente de trabalho:

```
$ git config --global user.name "Bruno Manarin"

$ git config --global user.email "bruno@manarin.xyz"`
```

Substitua os textos pelo seu nome e e-mail.

## Terceira etapa:

Temos agora o seu repositório do GitHub pronto e o Git configurado no seu computador, falta só juntarmos os dois!
Para isso, crie uma nova pasta na sua área de trabalho, chamaremos de Primeiro repo.

![git-folder](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/git-folder.png)


#### Ubuntu:

Abra e pasta e clique com o botão direito dentro, em seguida acesse a opção "Open in terminal".

![git-open-terminal](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/git-open-in-terminal.png)

Assim que o terminal abrir digite:

`$ git init`

Este comando serve para iniciar um repositório em seu computador. Toda vez que você criar um novo projeto irá utilizá-lo. 

![git-terminal](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/git-terminal.png)

Abra agora seu editor de texto preferido e copie o seguinte padrão:

```
# Olá, meu nome é {seu nome aqui}
## Este é meu primeiro repositório.

### Eu entrei no curso de {seu curso aqui} pois:
{motivo aqui}
### Minhas atividades preferidas são:
{atividades aqui}

```

Após substituir as lacunas, salve o arquivo na pasta "Primeiro repo" com o nome de README.md.

Volte ao terminal e digite:

`$git status`

O comando status mostra como está o git no momento, ou seja, mostrará que arquivos fazem parte do projeto e quais não.

Você vai ver que o arquivo README.md foi encontrado e vai estar destacado em vermelho:

![git-red](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/git-red.png)

Isso significa que ele foi encontrado na pasta, porém ainda não faz parte do nosso projeto.

Utilize o comando:


`$ git add README.md`


Para adicionar o arquivo ao projeto e na fila para o primeiro commit.


*Toda vez que você for adicionar um arquivo, você deve utilizar o comando add seguido do nome dele*

`$ git add [NOME DO ARQUIVO AQUI]`

*Você pode também adicionar a pasta inteira usando um "."*

`$ git add .`

*Isso permite que todos os arquivos daquela pasta sejam adicionados ao projeto atual.*

Digite agora o comando status de novo para checar se tudo deu certo:

`$git status`

Agora o README.md deve estar verde.

![git-green](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/git-green.png)

Finalmente vamos ao nosso primeiro Commit!

`$ git commit -m "Meu primeiro Commit"`

O comando commit serve como uma espécie de confirmação, ele afirma que aquele(s) arquivo(s) estão prontos para o repositório. É importante ressaltar que a parte do -m (message) é muito importante! Ela indica o que é o commit e é obrigatória.

Agora que temos tudo preparado, vamos mandar para o GitHub!

![github-first-repo](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/github-setup-repo.png)

Lembra dessa tela aqui? Pois é! Copie o link disponível na caixa de texto e cole o no seu console:

`$ git remote add origin [LINK AQUI]`

Esse comando linkará o Git (Sua máquina local) ao GitHub (Situado na internet) e possibilitará a transferência de arquivos entre os dois!

Último passo é só dar o push no arquivo:

`$ git push -u origin master`

Push (Empurrar em português) é um comando usado para mandar as modificações locais para o repositório on-line. Os outros parâmetros que seguem indicam que é a primeira vez que o repositório está sendo iniciado. Nas seguintes vezes que você for usar o comando nesse repositório, utilize apenas:

`$ git push`

Já que o repositório já se encontra configurado.

Seu resultado deve ser esse:

![github-finished](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/github-finished.png)


Parabéns! Você iniciou seu primeiro repositório GitHub!

### Windows:

Abra e pasta e clique com o botão direito dentro, em seguida acesse a opção "Git Bash here".

![git-open-terminal-windows](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/git-windows-bash-here.jpg)

Assim que o GitBash abrir digite:

`$ git init`

Este comando serve para iniciar um repositório em seu computador. Toda vez que você criar um novo projeto irá utilizá-lo. 

![git-terminal-windows](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/git-windows-init.png)

Abra agora seu editor de texto preferido (pode ser o bloco de notas) e copie o seguinte padrão:

```
# Olá, meu nome é {seu nome aqui}
## Este é meu primeiro repositório.

### Eu entrei no curso de {seu curso aqui} pois:
{motivo aqui}
### Minhas atividades preferidas são:
{atividades aqui}

```

Após substituir as lacunas, salve o arquivo na pasta "Primeiro repo" com o nome de README.md.
**Não esqueça de mudar a opção de "Arquivo de texto" para "Todos arquivos" quando for salvar!**



Volte ao terminal e digite:

`$git status`

O comando status mostra como está o git no momento, ou seja, mostrará que arquivos fazem parte do projeto e quais não.

Você vai ver que o arquivo README.md foi encontrado e vai estar destacado em vermelho:

![git-red](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/git-red.png)

Isso significa que ele foi encontrado na pasta, porém ainda não faz parte do nosso projeto.

Utilize o comando:


`$ git add README.md`


Para adicionar o arquivo ao projeto e na fila para o primeiro commit.


*Toda vez que você for adicionar um arquivo, você deve utilizar o comando add seguido do nome dele*

`$ git add [NOME DO ARQUIVO AQUI]`

*Você pode também adicionar a pasta inteira usando um "."*

`$ git add .`

*Isso permite que todos os arquivos daquela pasta sejam adicionados ao projeto atual.*

Digite agora o comando status de novo para checar se tudo deu certo:

`$git status`

Agora o README.md deve estar verde.

![git-green](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/git-green.png)

Finalmente vamos ao nosso primeiro Commit!

`$ git commit -m "Meu primeiro Commit"`

O comando commit serve como uma espécie de confirmação, ele afirma que aquele(s) arquivo(s) estão prontos para o repositório. É importante ressaltar que a parte do -m (message) é muito importante! Ela indica o que é o commit e é obrigatória.

Agora que temos tudo preparado, vamos mandar para o GitHub!

![github-first-repo](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/github-setup-repo.png)

Lembra dessa tela aqui? Pois é! Copie o link disponível na caixa de texto e cole o no seu console:

`$ git remote add origin [LINK AQUI]`

Esse comando linkará o Git (Sua máquina local) ao GitHub (Situado na internet) e possibilitará a transferência de arquivos entre os dois!

Último passo é só dar o push no arquivo:

`$ git push -u origin master`

Push (Empurrar em português) é um comando usado para mandar as modificações locais para o repositório on-line. Os outros parâmetros que seguem indicam que é a primeira vez que o repositório está sendo iniciado. Nas seguintes vezes que você for usar o comando nesse repositório, utilize apenas:

`$ git push`

Já que o repositório já se encontra configurado.

Seu resultado deve ser esse:

![github-finished](https://raw.githubusercontent.com/brunomanarin/yourfirstgihubrepo/master/img/github-finished.png)

Parabéns, você agora tem um repositório GitHub!

## Considerações Finais:

No tutorial de hoje você aprendeu:

Comandos gerais do Git (commit,push,init, add);
Conceitos gerais da ferramenta;
Repositórios do github;
Criação e manipulação de arquivos através do git.

Muito obrigado pela atenção!

## Observações:

Fico a disposição pessoalmente ou pelo e-mail brunomanarin@icloud.com para sanar qualquer dúvida.

Creio que podem existir bugs na versão do windows (GitBash), sugiro que comecem a usar o ubuntu o mais rápido o possível! (Não é tão difícil!). Caso ocorra, tente digitar o comando ao invés de copiar/colar na tela do GitBash ou usar a própria prompt de comando do Windows.

## Links interessantes:

[FreeCodeCamp - Git](https://guide.freecodecamp.org/git/) -> Contém várias informações interessantes sobre a ferramenta.

[Guia de Sintaxe para escrever READMEs](https://help.github.com/en/articles/basic-writing-and-formatting-syntax)

[Básicos do GitBash](https://www.youtube.com/watch?v=oQc-2gsjgDg) -> Útil também para aprender alguns comandos do terminal 
Linux

[Git e GitHub em 30 minutos](https://www.youtube.com/watch?v=SWYqp7iY_Tc)











