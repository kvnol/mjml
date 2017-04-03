
# Layout Básico

Neste seção, você vai aprender como fazer o código de um modelo de e-mail básico utilizando MJML.

Aqui está o resultado que queremos alcançar no final:

<p align="center">
  <a href="http://mjml.io/try-it-live/templates/hello-world"><img width="350px" src="https://cloud.githubusercontent.com/assets/6558790/12779864/d9c20556-ca6a-11e5-9007-d40ac89c5088.png" alt="sexy"></a>
</p>

<p align="center">
  <a href="/try-it-live/templates/basic"><img width="100px" src="http://imgh.us/TRYITLIVE.svg" alt="sexy" /></a>
</p>

Legal, não é?

## Seções

``` html
<mjml>
  <mj-body>
    <mj-container>

      <!-- Cabeçalho da Empresa -->
      <mj-section background-color="#f0f0f0"></mj-section>

      <!-- Imagem do cabeçalho -->
      <mj-section background-color="#f0f0f0"></mj-section>

      <!-- Texto de Introdução -->
      <mj-section background-color="#fafafa"></mj-section>

      <!-- Seção com 2 colunas -->
      <mj-section background-color="white"></mj-section>

      <!-- Ícones -->
      <mj-section background-color="#fbfbfb"></mj-section>

      <!-- Ícones Sociais -->
      <mj-section background-color="#f0f0f0"></mj-section>

    </mj-container>
  </mj-body>
</mjml>
```

Primeiramente, nós vamos implementar o esqueleto que são as seções. Aqui, nosso e-mail será divido em 6 seções.

## Cabeçalho da Empresa

``` html
<!-- Cabeçalho da Empresa -->
<mj-section background-color="#f0f0f0">
  <mj-column>
    <mj-text  font-style="italic"
              font-size="20"
              color="#626262">
      Minha Empresa
    </mj-text>
  </mj-column>
</mj-section>

```

A primeira seção do e-mail consiste num banner centralizado, contendo apenas o nome da empresa. A seguinte marcação é a representação, em MJML, do modelo que nós queremos obter.

<aside class="notice">
  Lembre de tudo que tem de estar contido em uma coluna.
</aside>

O padding do texto representa o espaço interno em volta do conteúdo sem o elemento `mj-text`

## Imagem do Cabeçalho

``` html
<!-- Image Header -->
  <mj-section background-url="http://1.bp.blogspot.com/-TPrfhxbYpDY/Uh3Refzk02I/AAAAAAAALw8/5sUJ0UUGYuw/s1600/New+York+in+The+1960's+-+70's+(2).jpg"
              background-size="cover"
              background-repeat="no-repeat">

    <mj-column width="600">

      <mj-text  align="center"
                color="#fff"
                font-size="40"
                font-family="Helvetica Neue">Slogan here</mj-text>

      <mj-button background-color="#F63A4D"
                 href="#">
        Promotion
      </mj-button>

    </mj-column>

  </mj-section>
```

O próximo vem numa seção com uma imagem de fundo, um bloco de texto (representando o slogan da empresa) e um botão apontando para uma páginas que lista todas as promoções da empresa.

Para adicionar uma imagem no cabeçalho, você terá que substituir o `background-color` pelo `background-url`.

Da mesma forma que ao primeiro cabeçalho, você terá um texto centralizado verticalmente e horizontalmente.

O padding continuará o mesmo.

O atributo `href` do `mj-button` define para o onde o botão apontará.

Para ter o fundo do cabeçalho com a largura máxima, defina a largura do `mj-column` para 600px com `width="600"`.

## Texto de Introdução

``` html
<!-- Texto de Introdução -->
  <mj-section background-color="#fafafa">
      <mj-column width="400">

          <mj-text font-style="italic"
                   font-size="20"
                   font-family="Helvetica Neue"
                   color="#626262">Meu texto incrível</mj-text>

          <mj-text color="#525252">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin rutrum enim eget magna efficitur, eu semper augue semper. Aliquam erat volutpat. Cras id dui lectus. Vestibulum sed finibus lectus, sit amet suscipit nibh. Proin nec commodo purus. Sed eget nulla elit. Nulla aliquet mollis faucibus.
          </mj-text>

          <mj-button background-color="#F45E43"
                     href="#">Leia mais</mj-button>

    </mj-column>
  </mj-section>
```

O texto de introdução consistirá do título, o texto principal e um botão.
O título é um `mj-text` normal que pode ser customizado.

## Seção de 2 colunas

``` html
<!-- Imagem lateral -->
<mj-section background-color="white">

  <!-- Imagem à esquerda -->
  <mj-column>
    <mj-image width="200"
              src="https://designspell.files.wordpress.com/2012/01/sciolino-paris-bw.jpg" />
  </mj-column>

  <!-- Parágrafo à direita -->
  <mj-column>
    <mj-text font-style="italic"
             font-size="20"
             font-family="Helvetica Neue"
             color="#626262">
        Ache lugares incríveis
      </mj-text>

      <mj-text color="#525252">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin rutrum enim eget magna efficitur, eu semper augue semper. Aliquam erat volutpat. Cras id dui lectus. Vestibulum sed finibus lectus.</mj-text>
  </mj-column>
</mj-section>
```

As seções são feitas de 2 colunas. Uma contém uma imagem e a outra contém um texto.
Para a coluna da imagem, note que quando a tag não possui um filho, você pode usar a sintaxe de XML:
`<mj-image />`

Para a coluna do texto, você vai precisar de dois `<mj-text>` como mostrado acima. Um com o formato do título e o outro como um texto normal.

## Ícones

``` html
<!-- Ícones -->
<mj-section background-color="#fbfbfb">
  <mj-column>
    <mj-image width="100" src="http://191n.mj.am/img/191n/3s/x0l.png" />
  </mj-column>
  <mj-column>
    <mj-image width="100" src="http://191n.mj.am/img/191n/3s/x01.png" />
  </mj-column>
  <mj-column>
    <mj-image width="100" src="http://191n.mj.am/img/191n/3s/x0s.png" />
  </mj-column>
</mj-section>
```

Esta seção é feita com 3 colunas. Por favor, observe que você pode alterar o espaço em torno das imagens com o atributo `padding`.

## Ícones sociais

``` html
<mj-section background-color="#e7e7e7">
  <mj-column>
      <mj-social display="facebook" />
  </mj-column>
</mj-section>
```

A biblioteca de componentes do MJML conta com o `mj-social`. Por padrão, todas as redes sociais são habilitadas. Para desabilitar algum deles, apenas use o nome da rede social como atributo com o valor `false`. Aqui, no exemplo acima, nós vamos usar apenas o `facebook`.