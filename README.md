# Repositório de Testes e comandos Git
Esse arquivo tem como objetivo reforçar, ensinar e clarear na minha mente 
alguns conceitos de versionamento de código.

## Apresentação dos Conceitos:
Estou usando guias de git muito bons em inglês que ensinam
toda a metodologia e conceito de git, vindos do tutorial no site Devtools [aqui.](https://dev.to/gothamv/learn-the-basics-of-git-in-under-10-minutes-475c)

Todos os comandos aqui listados serão apresentados com
técnicas de formatação(*markdown*) vindas do próprio 
[Github Guides!](https://guides.github.com/features/mastering-markdown/) Um tipo de ferramenta que é muito valiosa para versionamento também.

## Primeiros passos e lista de comandos:

#### 0. Faça download do GIT (caso não tenha)
Você precisará desse programa, pois ele é justamente o programa controlador de versão. Caso você use windows, vá até esse [link](https://git-scm.com/download/win) para download **`instantâneo`** do mesmo.

Verifique no seu prompt de comando, com o comando **git --version** se o git foi instalado. Caso afirmativo, aparecerá o número da versão, caso contrário o windows simplesmente avisará que não há nenhum comando dessa natureza registrado.

#### 1. Crie um repositório no Github
Crie um repositório vazio no github para futuramente usá-lo para sincronizar um diretório dentro do seu computador a ele, e assim fazer seu esquema de controle de versão linkado ao seu github. 

#### 2. Torne um diretório do seu coputador num diretório GIT 

#### `AVISO:`
#### `O principal começa aqui.`

Vá dentro da pasta ao qual você deseja transformar no seu repositório local dentro do seu PC. Por meio do cmd (prompt de comando); vá dentro dela, usando o comando **cd nome_da_pasta** e digite o comando **git init** dentro dela.

Isso fará com que seu PC reconheça essa pasta como um repositório local GIT.

#### 3. **Identifique-se como usuário GIT**

Diga ao sistema de versionamento quem você é, isso é vital para todo o histórico de mudança de arquivos, pois informa quem é o responsável pelas tais mudanças. Recomendo usar seu nome do Github e o seu email do Github também.

Para fazer isso, digite dentro do prompt:

<div>
  - <strong>git config --global user.name</strong> "seu nome do github"
</div>
<div> 
  - <strong>git config --global user.email</strong> "seu email do github"
</div>
<div> 
  - <strong>git config --global --list</strong> | Mostrará as informações que você digitou.
</div>



#### 4. **git add**
Agora você finalmente inicializou sua pasta como um repositório local dentro do seu PC, e já existe um repositório no Github esperando para se conectar  com este seu projeto aqui na sua máquina. Nós já podemos fazer algo.

De maneira normal, você pode criar, editar e excluir arquivos aqui dentro da sua pasta. Mas eles não estarão sendo rastreados de imediato pelo sistema de versionamento. Isso significa que qualquer alteração neles será tratada como qualquer outra em alguma pasta aleatória do seu computador.

Para ativar essa funcionalidade é necessário um dos seguintes comandos:

- Variações:
  - **git add** *nome_arquivo_escolhido*
Adiciona o arquivo escolhido dentro do seu diretório git, à lista de espera (ou lista de arquivos rastreados / *git staged files*) para serem **commitados futuramente** (resumindo, agora o sistema está de olho neles 👀). E sempre que você mudar alguma coisa neles, ou apagá-los, isso será registrado.

  - **git add .**
Adiciona todos os arquivos e pastas dentro do seu diretório git a lista de espera para serem commitados. Também conhecida como *git staged files waiting for commit*.
  - **git restore --staged** nome_arquivo
Caso você não queira mais que o seu arquivo escolhido seja rastreado e esteja na lista de espera, digite isso e ele voltará a ser só um arquivo comum.

#### 5. **git status**