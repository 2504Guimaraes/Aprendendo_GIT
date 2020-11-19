# Repositírio de Testes e comandos Git
Esse arquivo tem como objetivo reforçar, ensinar e clarear na minha mente 
alguns conceitos de versionamento de código.

## Apresentação dos Conceitos:
Estou usando guias de git muito bons em inglês que ensinam
toda a metodologia e conceito de git, vindos do tutorial no site Devtools [aqui.](https://dev.to/gothamv/learn-the-basics-of-git-in-under-10-minutes-475c)

Todos os comandos aqui listados serão apresentados com
técnicas de formatação(*markdown*) vindas do próprio 
[Github Guides!](https://guides.github.com/features/mastering-markdown/)

## Primeiros passos e lista de comandos:

#### 0. Faça download do GIT (caso não tenha)
Você precisará desse programa, pois ele é justamente o programa controlador de versão. Caso você use windows, vá até esse [link](https://git-scm.com/download/win) para download.

Verifique no seu prompt de comando com o comando **git --version** se o git foi instalado. Caso sim aparecerá o número da versão, caso contrário o windows simplesmente avisará que não há nenhum comando dessa natureza registrado.

#### 1. Crie um repositório no Github
Crie um repositório vazio no github para futuramente usá-lo para sincronizar 
um diretório dentro do seu computador a ele, e assim fazer seu esquema de controle de versão. 

#### 2. Torne um diretório do seu coputador num diretório GIT 

#### `AVISO - Comandos GIT começam aqui.`

Vá dentro da pasda desejada para se tornar seu repositório local do seu PC
por meio do cmd. Dentro dela digite o comando **git init**.

Isso fará com que seu PC reconheça agora esapasta como um repositório local GIT.

#### 3. **git add**
- Variações:
  - **git add** *nome_arquivo_desejado*
Adiciona o arquivo escolhido dentro do seu diretório git, à lista de espera (ou lista de arquivos rastreados / *git staged files*) para serem commitados.
  - **git add .**
Adiciona todos os arquivos e pastas dentro do seu diretório git a lista de espera para serem commitados. Também conhecida como *git staged files waiting for commit*.