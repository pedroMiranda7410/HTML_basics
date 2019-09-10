HEAD TAG
    A tag <head> engobla os elementos que não serão "visualizados" na página da sua aplicação, os navegadores por padrão incluem
    um css para as tags <head> com um "display: none":

        head{
          display:none;
        }

    Os seguintes elementos sãos as tags que podem ser inseridas na tag <head>:

        <title> (this element is required in an HTML document)
        <style>
        <base>
        <link>
        <meta>
        <script>
        <noscript>


  1° Title Tag <title>

    É o que irá aparecer na aba do seu navegador (<title>Esse é meu site</title>)

  2º Style Tag <style>

    Dentro dela você consegue colocar códigos CSS's que só serão lidos na página onde a tag for inserida

  3° Base Tag <base>

    O Elemento HTML Base (<base>) especifica o endereço (URL) utilizada por todos os endereços relativos contidos dentro de um documento. Há um número máximo de 1 (um) elemento Base <base> do documento.

  4° link Tag <link>

    A tag <link> define um link entre um documento e um recurso externo. É usada para vincular a folhas de estilos (Style sheets), ou arquivos css, externas.

  5° Meta Tags <meta>

    Metadados são dados (informações) sobre dados.

    A tag <meta> fornece metadados sobre o documento HTML. Os metadados não serão exibidos na página, mas serão analisados ​​por máquina,nos quaism serão
    usados ​​para especificar a descrição da página, as palavras-chave, o autor do documento, a última modificação e outros metadados.
    Resumidamente falando: Todas as palavras chave que serão usados por navegadores como mecanismo de pesquisa e dispostos ao ter finalizado a pesquisa, por exemplo
    pesquisar "esquilos" no google, se você colocar a seguinte tag <meta name="description" content="Esquilos são legais">, sua página irá aparecer na pesquisa.


  6º Script Tag <script>

    O Elemento HTML <script> é usado para incluir ou referenciar um script executável.

  7° Noscript Tag <noscript>

    O Elemento HTML <noscript> define uma seção de html a ser inserida se um tipo de script não é suportado pela página ou se o script está desativado no navegador.
