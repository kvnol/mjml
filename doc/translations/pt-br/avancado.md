
# Layout da Newsletter

Neste seção, você vai criar um modelo de newsletter. O resultado final se parecerá com isso:

<p align="center">
  <a href="/try-it-live/templates/hello-world"><img width="350px" src="https://cloud.githubusercontent.com/assets/6558790/12789753/6fd35f3e-ca9f-11e5-8ff0-a1e090a9bede.png" alt="sexy"></a>
</p>

<p align="center">
  <a href="/try-it-live/templates/newsletter"><img width="100px" src="http://imgh.us/TRYITLIVE.svg" alt="sexy" /></a>
</p>

## Estrutura

``` html
<mjml>
  <mj-body>
    <mj-container>

      <!-- Cabeçalho -->
      <mj-section></mj-section>

      <!-- Banner -->
      <mj-section></mj-section>

      <!-- Artigo -->
      <mj-section></mj-section>

      <!-- Cabeçalho do Editor -->
      <mj-section></mj-section>

      <!-- Editor da Imagem -->
      <mj-section></mj-section>

      <!-- Artigo -->
      <mj-section></mj-section>

      <!-- Social -->
      <mj-section></mj-section>

    </mj-container>
  </mj-body>
</mjml>
```
Da mesma forma que o layout básico acima, você terá que, primeiro, dividir o seu modelo em seções.

## Cabeçalho

``` html
<!-- Cabeçalho -->
<mj-section padding-bottom="0" background-color="white">
  <mj-column width="100%">
    <mj-image src="https://avatars0.githubusercontent.com/u/16115896?v=3&s=200" width="50px"/>

      <mj-divider
          padding-top="20"
          padding-bottom="0"
          padding-left="0"
          padding-right="0"
          border-width="1px"
          border-color="#f8f8f8"/>
  </mj-column>
</mj-section>
```

O cabeçalho pode ser, facilmente, feito com o `mj-image`. Queremos que uma fina borda seja adicionada com um `mj-divider`. Este componente age como uma borda CSS.

Observe que alguns componentes como o `mj-section` e `mj-divider` vem com valores padrões para o padding.

## Banner

``` html
<!-- Banner -->
<mj-section padding-bottom="0" background-color="#fcfcfc">
  <mj-column width="100%">
    <mj-text align="center" font-size="20" color="grey" font-family="Helvetica Neue" font-weight="200">
    Aqui está o que você perdeu.
      </mj-text>
      <mj-divider
          padding-top="20"
          padding-bottom="0"
          padding-left="0"
          padding-right="0"
          border-width="1px"
          border-color="#f8f8f8"/>
  </mj-column>
</mj-section>
```

Para o banner, queremos o mesmo divisor com um `mj-text`.

## Artigo

A coluna de artigo precisa ter um tamanho definido manualmente. Por padrão, os valores são considerados em pixels.
A primeira coluna contém uma imagem, enquanto a segunda contém um título e um parágrafo. Os dois `mj-text` são alinhados à esquerda.

## Editor

``` html
<!-- Editor -->
<mj-section padding-bottom="0">
  <mj-column>
    <mj-text font-size="20" color="rgb(165, 176, 184)">
        Explore nossos novos recursos.
      </mj-text>
  </mj-column>
</mj-section>

<mj-section padding-top="0">
  <mj-column width="600">
    <mj-image src="https://cloud.githubusercontent.com/assets/6558790/12450760/ee034178-bf85-11e5-9dda-98d0c8f9f8d6.png"/>
  </mj-column>
</mj-section>
```

Note que, neste exemplo, as cores podem ser expressadas utilizando diferentes formatos (rgb, hsl, hex etc.).

## Social

``` html
<mj-section background-color="#f3f3f3">
  <mj-column>
    <mj-text>Mantenha contato!</mj-text>
      <mj-social
          mode="vertical"
          display="twitter facebook" />
  </mj-column>
</mj-section>
```

Finalmente, como em nosso exemplo anterior, a parte para os ícones sociais (`mj-social`) serão alinhadas verticalmente.