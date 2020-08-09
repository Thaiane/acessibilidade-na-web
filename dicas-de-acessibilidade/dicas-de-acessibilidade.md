# Dicas de acessibilidade web

* Declarar a linguagem do documento. É importante para o leitor saber qual linguagem do site.

* Ter um `<h1>` na página declarando o título da página.

* Fazer a divisão adequada dos textos com títulos usando tags `html`.

* Sempre associar `<label>` aos controles de formulário.

* Usar adequadamente a semântica dos elementos HTML.

* Jamais remova o outline dos elementos CSS. Isso faz com que perdemos o foco de onde está o `tab`.

* Não basta estilizar o `:hover`, estilize o `:focus` também. Mobile só tem `:focus` por exemplo.

*Testos capitalizadosou em caixa-alta SEMPRE em `css` nunca `html`. Dessa forma vai manter a visualização
e nao impactar no leitor de tela.

* Toda imagem precisa ter um `alt` associado para descrever a imagem. E descrever de forma simples e essencial. Isso ajuda no SEO também.

* Marque o ínicio do conteúdo e adicione um link para ele. Isso já vira um atalho para ir direto ao conteúdo. Se possível primeiro link da página.

* Marque os ``landark roles`` do aria. Alguns leitores de tela usam isso para navegar:

``` 
    header role="banner">
    
    <nav role="navigation">
    
    <div id="conteudoprincipal" role="main">
    
    <div id="widget" role="complementary">
    
    <form action="search.php" role="search">
    
    <p class="copyright" role="contentinfo">
```

* Não use ``clique aqui`` para links. Os textos dos links não fazem sentido para quem varre o site pelos links.

* Assegura contraste adequado entre fonte e cores/imagem de fundo. Usar ``background-color`` também no container para caso a imagem não carregue.

* Não associar informações somente a cores.

* Tste seu site com CSS e Javascript desabilitado. Veja se o HTML está fazendo sentido.

* Considere diferentes contexto de uso: idade, deficiencias...

Fonte: (palestra da Talita)[https://www.youtube.com/watch?v=4URTZHk6tz0]
* https://uxmag.com/articles/15-website-accessibility-tips-that-increase-everyone%E2%80%99s-engagement
* https://www.webfx.com/blog/web-design/10-simple-web-accessibility-tips-you-can-do-today/
* https://webdesign.tutsplus.com/articles/6-tips-for-improving-website-accessibility--webdesign-1660
* https://webaccess.berkeley.edu/resources/tips/web-accessibility