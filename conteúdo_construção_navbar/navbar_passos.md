* Replicando o site da rocketseat

* Passo a passo
- inicie o arquivo .HTML com o seguinte código:

  <!DOCTYPE html>
  <html lang="en" dir="ltr">
    <head>
      <meta charset="utf-8">
      <title></title>
    </head>
    <body>

    </body>
  </html>

  - Em seguida, antes da Tag body, por questões de organização e padrão, crie a tag <header> ... </header> para colocarmos a barra de navegação.

  <!DOCTYPE html>
  <html lang="en" dir="ltr">
    <head>
      <meta charset="utf-8">
      <title></title>
    </head>

    <header>

    </header>

    <body>

    </body>
  </html>

- Como na barra de navegação nós só queremos colocar os caminhos que iremos percorrer dentro do site, vamos separa-las por <div>'s para melhor estruturação, ficará assim:

  <header>
    <div>
      <nav>
        <a>Imagem</a>
        <ul>
          <li>Início</li>
          <li>Starter</li>
          .
          .
          .
        </ul>
      </nav>
      <div>
        <a>Instagram</a>
        <a>Facebook</a>
        .
        .
        <a class="login-btn">Login</a>
      </div>
    </div>    
  </header>

- Dentro da tag <nav> temos nossa navegação dentro do site e os demais são links de conteúdos separados.
- Agora vamos dar um embelezamento á nossa estruturação com um pouco de css. Então vamos por partes iniciando pela tag principal que engloba todos os outros itens que é a tag <header>

  HTML -> <header class="header-css">

  CSS ->
          .header-css{
            width: 100%;
            height: 80px;
            color: rgb(255, 255, 255);
            background: rgb(113, 89, 193);
            transition: all 0.5s ease 0s;
          }

- Nós já conseguimos ver uma diferença inicial, vamos dar continuidade com a outra div que engloba os itens restantes para centralizá-los e dar o ar de que estão todos alinhados num mesmo plano:

  HTML ->     <header class="header-css">
                <div class="header-div width-adjust">

  CSS ->
            .header-div {
              height: 100%;
              display: flex;
              flex-direction: row;
              -webkit-box-pack: justify;
              justify-content: space-between;
              -webkit-box-align: center;
              align-items: center;
            }

            .width-adjust {
                max-width: 1070px;
                padding: 0px 30px;      /* padding left and right*/
                margin: 0px auto;
            }

- Agora que já ajustamos as posições de cada seção da nossa barra de navegação, vamos organizar os itens da lista que está dentro da tag <mav>. Iremos fazer os itens se posicionarem de forma reta em linha ( row )
Obs: para melhores explicações quanto ao css envolvendo display: flex, justify-content e tudo mais, acessar o site https://origamid.com/projetos/flexbox-guia-completo/

  HTML ->   <nav class="nav-styling ">
              <a href="#">IMG</a>
                <ul>
                  <li>
                    <a href="#">início</a>
                  </li>
                  <li>
                    <a href="#">Starter</a>
                  </li>
                  <li>
                    <a href="#">Bootcamp</a>
                  </li>
                  <li>
                    <a href="#">Comunidade</a>
                  </li>
                  <li>
                    <a href="#">Blog</a>
                  </li>
                </ul>
          </nav>

  CSS ->    

          .nav-styling{
            display: flex;
            flex-direction: row;
            -webkit-box-align: center;
            align-items: center;
          }

          .nav-styling ul{ /* esse espaçamento significa que quaisquer tag que tenha o css ".nav-styling", nesse caso, suas tags <ul> que estão dentro sofrerá as alterações impostas nesse css abaixo*/
              display: flex;
              flex-direction: row;
              -webkit-box-pack: justify;
              justify-content: space-between;
              -webkit-box-align: center;
              align-items: center;
          }

          .nav-styling ul{
            margin-block-start: 1em;
            margin-block-end: 1em;
            margin-inline-start: 0px;
            margin-inline-end: 0px;
            padding-inline-start: 40px;
          }

- Se você olha agora, vai ver que os itens ficaram alinhados, mas estão com bolas escuras representando os itens da lista, os links que levão pra outra página estão azulados e com uma linha embaixo e as caixas não se encostam totalmente no início da tela, parecendo que está faltando um espaço. Vamos concertar isso com os seguintes CSS's:

CSS ->

  /* Esse vai deixar todas as tags sem nenhum espaçãmento entre outras caixas, podendo ser trabalhadas para se separar separadamente com css's exclusivos pra cada tag */
    * {
        box-sizing: border-box;
        margin: 0px;
        padding: 0px;
        outline: 0px;
    }


    /* Aqui estamos tirando a estilização padrão dos links, tirando a barra de baixo das letras e mudando a cor da letra pra um branco indo levemente pro escuro/cinza */
    a {
      text-decoration: none;
      color: rgb(255, 255, 255);
    }

    /* Esse CSS retira a estilização padrão das tags <li> que são as bolinhas pretas */
    li{
      list-style-type: none;
    }

- Agora já conseguimos ver toda a estrutura da barra de navegação, faltando apenas dar alguns espaçamentos e trazer um embelezamento especial pra cada item
