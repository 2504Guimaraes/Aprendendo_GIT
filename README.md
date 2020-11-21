# Tutorial de comandos Git
**`nota:`** ` eu posso ter feito alguns testes de comandos para aprendizado aqui dentro.`

Esse arquivo tem como objetivo reforçar, ensinar e clarear na minha mente 
alguns conceitos de versionamento de código.

## Apresentação dos Conceitos:

Estou usando guias de git muito bons em inglês que ensinam
toda a metodologia e conceito de git, vindos do tutorial no site dev.to [aqui.](https://dev.to/gothamv/learn-the-basics-of-git-in-under-10-minutes-475c)

Todos os comandos aqui listados serão apresentados com
técnicas de formatação(*markdown*) vindas do próprio 
[Github Guides!](https://guides.github.com/features/mastering-markdown/) Um tipo de ferramenta que é muito valiosa para versionamento também.

## Primeiros passos e lista de comandos:

#### 0. Faça download do GIT (caso não tenha)

Você precisará desse programa, pois ele é justamente o programa controlador de versão. Caso você use windows, vá até esse [link](https://git-scm.com/download/win) para download **`instantâneo`** do mesmo.

Verifique no seu prompt de comando, com o comando **git --version** se o git foi instalado. Caso afirmativo, aparecerá o número da versão, caso contrário o windows simplesmente avisará que não há nenhum comando dessa natureza registrado.

#### 1. Crie um repositório no Github

Crie um repositório vazio no github para futuramente usá-lo para sincronizar um diretório dentro do seu computador a ele, e assim fazer seu esquema de controle de versão linkado ao seu github. 

#### 2. Torne um diretório do seu computador num diretório GIT 

#### `AVISO:`
#### `O principal começa aqui.`

Vá dentro da pasta ao qual você deseja transformar no seu repositório local dentro do seu PC. Por meio do cmd (prompt de comando); vá dentro dela, usando o comando **cd nome_da_pasta** e digite o comando **git init** dentro dela.

Isso fará com que seu PC reconheça essa pasta como um repositório local GIT.

#### 3. **Identifique-se como usuário GIT**


Diga ao sistema de versionamento quem você é, isso é vital para todo o histórico de mudança de arquivos, pois informa quem é o responsável pelas tais mudanças. Recomendo usar seu nome do Github e o seu email do Github também.

Para fazer isso, digite dentro do prompt:

<div>
  <strong>git config --global user.name</strong> "seu nome do github"
</div>
<div> 
  <strong>git config --global user.email</strong> "seu email do github"
</div>
<div> 
  <strong>git config --global --list</strong> | Mostrará as informações que você digitou.
</div>



#### 4. **git add**

Agora você finalmente inicializou sua pasta como um repositório local dentro do seu PC, e já existe um repositório no Github esperando para se conectar  com este seu projeto aqui na sua máquina. Nós já podemos fazer algo.

De maneira normal, você pode criar, editar e excluir arquivos aqui dentro da sua pasta. Mas eles não estarão sendo rastreados de imediato pelo sistema de versionamento. Isso significa que qualquer alteração neles será tratada como qualquer outra em alguma pasta aleatória do seu computador.

Para ativar essa funcionalidade é necessário um dos seguintes comandos:

- Variações:
  - **git add** *nome_arquivo_escolhido*
    - Adiciona o arquivo escolhido dentro do seu diretório git, à lista de espera (ou lista de arquivos rastreados / *git staged files*) para serem **commitados futuramente** (resumindo, agora o sistema está de olho neles 👀). E sempre que você mudar alguma coisa neles, ou apagá-los, isso será registrado.

  - **git add .**
    - Adiciona todos os arquivos e pastas dentro do seu diretório git a lista de espera para serem commitados. Também conhecida como *git staged files waiting for commit*.
  - **git restore --staged** nome_arquivo
    - Caso você não queira mais que o seu arquivo escolhido seja rastreado e esteja na lista de espera, digite isso e ele voltará a ser só um arquivo comum.

#### 5. **git status**

Digitando apenas **git status** dentro da sua pasta linkada ao git, você consegue saber quais arquivos estão sendo observados / em espera para poderem ser **commitados**. Ou novamente, como diz o termo técnico: "*git staged files*".

Esses arquivos aparecerão em uma lista simples em verde, esperando que você finalmente dê um commit (**que você ainda não deu, claro**) e *finalmente os registre como um novo degral no grupo de mudanças importantes do seu projeto* 😊.

#### 6. **git commit**

Agora finalmente chegamos nele! **git commit**!!! <h4>"Ele é o responsável por pegar toda aquela lista de arquivos sendo rastreados e registra-los oficialmente como uma mudança dentro da linha do tempo de desenvolvimento do seu projeto."</h4>

#### `Imagine comigo:`

Imaginando que eu criei, pus para rastrear mudanças (**git add**) e modifiquei 1 arquivo.html mais 2 arquivos.css dentro do meu projeto. Quando eu desse **git commit** após ter feito tudo isso, eu registraria todos esses passos importantes, e ainda adicionaria uma descrição para falar o quê eu fiz. No meu caso, eu pessoalmente escreveria:

#### `"Criação e modificação inicial de html e estilos."`

Ou na forma de comando:

#### `git commit -m "Criação e modificação inicial de html e estilos."`

Como pode imaginar **-m** vem de *message* ou mensagem.

Ou seja, a grande idéia é que cada **commit** representa um **bloco de mudanças marcantes que eu fiz em um determinado momento**.

- Variações:
  - **git commit -m** "título descritivo"
    - Quando você faz um **commit**, é **obrigatório** que você ponha um título descrevendo o quê você fez. Pois o grande propósito da coisa é justamente que outras pessoas que venham a ver seu código e que trabalham com você entendam o quê você fez e os seus motivos para isso naquele momento.
  - **git commit -m** "título" **-d** "parágrafo descritivo"
    - Esse é exatamente igual ao anterior só que dá a você alternativa a mais de ir um pouco além na descrição, porém é um pouco desconfortável pois o prompt de comando não permite quebra de linhas e fica difícil de escrever algo muito grande. 
  - **git commit**
    - #### `AVISO:`
    - ##### `Não é possível usar esse comando sem algumas exigências.`
    - Honestamente, esse daqui é o melhor comando de todos (ao menos para mim 😅) pois ele permite que quando eu der **commit**, meus commits tenham tanto títulos descentes do que eu mudei, quanto parágrafos bem definidos caso a mudança nos meus arquivos tenha sido muito grande ou complexa.
    - **Porém de imediato o prompt de comando não reconhece ele, e dará erro caso você só escreva git commit agora**. Para que o prompt do windows aceite essa variação, escreva no seu prompt a seguinte instrução:
    - #### ` git config --global core.editor "code --wait" `
    - Isso fará com que o VScode seja reconhecido como a ferramenta que te ajudará a escrever melhores descrições. 
    - **Finalmente**, assim que eu escrevo o comando **git commit**, o prompt ligará o VScode automaticamente, e me mostrará uma janela para eu poder escrever tanto o título do meu commit quanto o parágrafo descritivo. Se eu quiser, só o título mesmo.
    - Quando essa tela do VScode aparecer, ela terá textos escritos com hashtag (**#**) antes deles e eles não devem ser apagados. O quê você deve fazer é simplesmente escrever debaixo desses textos o seu título. Caso você quiser um parágrafo descritivo também, para fazer isso só dê um enter, pule uma linha e escreva-o.
    - Depois de escrever o quê você queria, salve-o pelo próprio VScode (**File > Save** ou **Ctrl + S**) e feche-o. Assim o prompt de comando que você havia deixado aberto para fazer isso que eu falei; exibirá a mensagem de que o seu **commit** foi devidamente registrado 😁😁.


#### 7. **git reset HEAD~1**
Esse comando é bem simples conceitualmente falando. Ele simplesmente desfaz o último **commit** feito por você. E sim, ele é case sensitive, logo escreva direitinho.

#### 8. **git remote**
Estamos chegando naquele momento onde finalmente iremos conectar seu projeto / repositório local no o seu repositório remoto lá no Github. E para fazermos essa ponte, obviamente você deve avisar ao seu git para onde você enviará todas essas informações. 

Para fazer isso use o comando:

#### `AVISO:`
#### `Versão principal do comando:`

- **git remote add** "apelido_branch_github" "url_branch_github"
- ##### Exemplo abaixo:
- **git remote add** `origin` https://github.com/nomeUsuario/SeuRepositorioGithub.git
- Deixando bem claro, **origin é o apelido que o seu repositório local dará ao galho (branch) do seu repositório remoto, aquele que fica lá no seu github**.
- Levando em conta que o git é uma linha do tempo que pode levar a várias versões alternativas; imagine que tudo isso é um grande árvore, a raiz é o início do universo e o tronco é a timeline principal. Além da linha do tempo principal, existem suas versões alternativas, que seriam galhos ou **branches** diferentes da nossa árvore. Você pode escolher qual em qual galho / timeline quer por suas atualizações, caso não queria ter o risco de comprometer o branch principal com algum erro, ponha em um alternativo.
- Escreva esse comando para adicionar um novo branch de um repositório remoto no github ao qual seu projeto será conectado e futuramente lançado (e sim, eu disse um novo pois dá pra conectar seu repositório local em mais de um branch de repositório remoto). Mas isso só fez a ponte, então calma, porque seu projeto ainda está na sua máquina.

#### `outras variações:`

- **git remote -v**
  - Mostrará todos as urls de repositórios branches remotos no github ao qual o seu repositório local tem conexão, junto dos respectivos apelidos deles.
- **git remote rm** apelido_branch_repositorio_remoto
  - Remove a conexão com algum branch remoto do github. Por exemplo; se eu não quisesse que meu projeto tivesse mais ligação com aquele branch do meu github ao qual eu apelidei de **origin**, eu simplesmente digitaria no meu prompt:
  - **git remote rm** origin
    - Isso simplesmente apagaria minha conexão com ele. Caso eu quisesse me conectar novamente; escreveria **git remote add...etc** de novo, e se eu quisesse poderia por até um outro apelido.

#### 8. **git push**
Agora finalmente, Iremos mandar os arquivos do seu repositório local até o seu repositório remoto 😁😁😁. Sendo bem direto, existem variacões desse comando (como tudo em git), bem, ai está finalmente o quê você usará para mandar seus arquivos ao seu repositório remoto:

  - **git push** **`apelido_branch_remoto`** **`nome_branch_local`**
    - Exemplo:
    - **git push** **`origin`** **`master`**
    - O quê acontece aqui, é que você está *empurrando* / *pushing* seus dados do seu branch local (**que por padrão se chama master**) até o branch escolhido por você (que já possui um apelido dado pelo seu git, no aqui foi apelidado de **origin**), que está lá no seu repositório remoto do Github.
    - E depois de todos esses detalhes, você **FINALMENTE** enviou seus dados até o seu Github! É isso ai 🤘.




