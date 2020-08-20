# Dicas de acessibilidade web

* Declarar a linguagem do documento. É importante para o leitor saber qual linguagem do site.

* Atributo ```<lang>``` é super importante para o leitor saber qual idioma do texto.

* Ter um `<h1>` na página declarando o título da página.

* Fazer a divisão adequada dos textos com títulos usando tags `html`.

* Sempre associar `<label>` aos controles de formulário.

* Usar adequadamente a semântica dos elementos HTML.

* Jamais remova o outline dos elementos CSS. Isso faz com que perdemos o foco de onde está o `tab`.

* Não basta estilizar o `:hover`, estilize o `:focus` também. Mobile só tem `:focus` por exemplo.

*Testos capitalizadosou em caixa-alta SEMPRE em `css` nunca `html`. Dessa forma vai manter a visualização
e nao impactar no leitor de tela.

* Toda imagem precisa ter um `alt` associado para descrever a imagem. E descrever de forma simples e essencial. 
Isso ajuda no SEO também e quando a imagem não carrega, o alt ajuda a fazer todos entenderem o que era a imagem.

* Se o alt tem valor apenas para visualização, então coloca alt vazio.``

* Marque o ínicio do conteúdo e adicione um link para ele. Isso já vira um atalho par`a ir direto ao conteúdo. Se possível primeiro link da página.

* Para colocar videos de forma mais acessivel use as tags html5: 

```
        <video src="img/formacao-java.mp4" class="secaoInstitucional-video" controls>
          <track src="img/legenda-portugues-brasil.vtt" kind="subtitles" srclang="pt-br" label="Português">
        </video>
```

* Uma forma de manter botões descritivos sem ferir o design é usar um span escondido:

```
          <button class="btnPadrao secaoPlanos-plano-btn">
            Assinar plano <span class="escondeVisualmente">Start por R$ 500,00</span>
          </button>
```
* Marque os ``landark roles`` do aria. Alguns leitores de tela usam isso para navegar:

``` 
    header role="banner">
    
    <nav role="navigation">
    
    <div id="conteudoprincipal" role="main">
    
    <div id="widget" role="complementary">
    
    <form action="search.php" role="search">
    
    <p class="copyright" role="contentinfo">
```

* Esse site possui todas as `rolas` que tem disponiveis: https://www.w3.org/TR/using-aria/#intro

* Não use ``clique aqui`` para links. Os textos dos links não fazem sentido para quem varre o site pelos links.

* Assegura contraste adequado entre fonte e cores/imagem de fundo. Usar ``background-color`` também no container para caso a imagem não carregue.

* Não associar informações somente a cores.

* Podemos usar o <desc>` ou `<longdesc>` para descrever.

* Use o title para descrever o svg, entretando isso nao funciona para todos os navegadores.

* Exemplo de imagem de logo com link: 
```<a href="#"><img src="img/10-aplicativos-mais baratos.png" alt= "Vai para algum lugar></a>```

* Teste seu site com CSS e Javascript desabilitado. Veja se o HTML está fazendo sentido.

* O CSS pode afetar a acessibilidade. Por exemplo, o elemento <ul> deve ser usado com a declaração
`list-style: none;` para evitar que o leitor leia "bolinha". Detalhes abaixo:

```
.secaoPlanos-plano-itens {
    text-align: left;
    padding-left: 30px;
    margin: 1em auto 1.5em auto;
    line-height: 2;
    list-style: none; // antes era desc, mas ai o leitor ficava lendo "bolinha" para cada item
    color: #666;
    width: 240:
}
```

* Para constraste de cores podemos verificar em sites de ```contraste check```.

* Sobre figuras, podemos usar o ``<figure>`` para marcar uma foto e o elemento `<figcaption>` 
para definir a legenda da foto/figura:
```
<figure>
   <img src="pic_trulli.jpg" alt="Trulli" style="width:100%">
   <figcaption>Fig.1 - Trulli, Puglia, Italy.</figcaption>
</figure>
```
* Use o ``for`` e `id` para linkar o label com um input, assim será possível ouvir a label
 quando for preencher um formulario.
 
* Prefira ``readonly`` no lugar de `disabled` em campos de formularios. Isso porque o desabilitado
não informa ao leitor de tela que esse campo é somente leitura.

* Sobre Wai-aria acesse a [documentação](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/WAI-ARIA_basics#What_is_WAI-ARIA)

* Considere diferentes contexto de uso: idade, deficiencias...

* Ótimo guia e acessibilidade é o [a11y style guide](https://a11y-style-guide.com/style-guide/).

* Artigo [11 dicas e boas práticas para deixar seu site acessível.](http://blog.handtalk.me/acessibilidade-ranking-google/)

Fonte: [palestra da Talita](https://www.youtube.com/watch?v=4URTZHk6tz0)
* https://uxmag.com/articles/15-website-accessibility-tips-that-increase-everyone%E2%80%99s-engagement
* https://www.webfx.com/blog/web-design/10-simple-web-accessibility-tips-you-can-do-today/
* https://webdesign.tutsplus.com/articles/6-tips-for-improving-website-accessibility--webdesign-1660
* https://webaccess.berkeley.edu/resources/tips/web-accessibility
* https://wave.webaim.org/
* https://achecker.ca/checker/index.php
* https://elo7.dev/um-pouco-sobre-css-js-a11y/
* https://webaim.org/techniques/keyboard/#testing