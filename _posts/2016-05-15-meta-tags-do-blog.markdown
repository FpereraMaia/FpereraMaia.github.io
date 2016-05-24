---
layout: post
autor: felipeQuadros
title: O que são meta tags HTML e quais utilizarei nesse blog?
categories: meta-tags html front-end
keywords: html, meta tags, microdata, front-end, SEO,HTML5, http, http-equiv, w3c
date:   2016-05-15 20:15:00 -0300
section: HTML
cervejaDoDia: Latão de Skol
linkCerveja: http://www.skol.com.br/produtos/lata-550ml-19
---

É isso mesmooo, temos nosso primeiro artigo, e será sobre meta tags!! Mas por quê? Por que eu to indo criar as meta tags desse blog agora, e após fuçar o [blog do akita](http://www.akitaonrails.com/) e o [blog do dinossauro das CSS](http://www.maujor.com) nota-se claramente que há meta tags pra caramba no mundo e eu não posso ficar aqui parado.

Só um minuto que esqueci o latão de skol.... Pronto, simbora.

## Beleza fera, mas o que são meta tags?
Segundo a wiki do [W3C](https://www.w3.org/wiki/HTML/Elements/meta) meta tags são:
"The <meta> element represents various kinds of metadata that cannot be expressed using the title, base, link, style, and script elements."
**Em HuehueBR** - Segundo o W3C (2012), o elemento <meta> representa uma variedade de metadados que não podem ser expressados usando os elementos title, base, link, style e script.

Ou seja, várias informações sobre a sua página serão declaradas em tags <meta>, **o que implica dizer que ela trabalha com metadados** e onde suponho surgiu o nome dessa tag.
Sendo assim, utilizaremos as meta tags para "informar informações" relativas ao nosso site, para facilitar o trabalho de um tanto de gente, como - por exemplo - do [facebook](https://www.facebook.com/felipepereira.quadrosmaia), que utiliza das informações colocadas por você (desenvolvedor) nas tag meta para apresentar uma publicação de uma página de forma linda e agradável - com imagens, descrições e o escambaul - na timeline.

Normalmente - eu disse **NORMALMENTE** - a tag <meta> tem dois atributos, um atributo define o funcionamento da tag meta e o outro atributo o conteúdo dessa tag. Beleza, tô confuso, vamos mostrar. Quando eu digo definir, isso quer dizer que dependendo do atributo declarado saberemos qual é o tipo do metadado que está no abributo de conteúdo. Sendo assim temos os atributos:

- **name** que quando está sendo utilizado é um metadado a nível de documento, por ex:
{% highlight html %}
<meta name="description" content="Meta tag que traz a descrição da sua página
e comumente utilizada pelo google para dar uma prévia sobre
as páginas no resultado da busca" />
<!-- Os SEO pira -->
{% endhighlight %}

- **http-equiv** quando declarado, é utilizado para simular um cabeçalho de resposta HTTP com o intuito de controlar as ações do browser. Ele não serve para sobrescrever a resposta HTTP do servidor. Um exemplo seria controlar o ato de cachear a página:
{% highlight html %}
<meta http-equiv="cache-control" content="no-cache" />
{% endhighlight %}

- **itemprop** vem de uma parada muito louca chamada [microdata](https://www.w3.org/TR/microdata/#content-models) do HTML5 que pode ser tema de uma próxima conversa. Quando setado em uma tag meta você pode omitir o atributo name, http-equiv e charset e é obrigatório ter o content. O google utiliza esses metas, por exemplo, no google plus "para apresentar uma publicação de uma página de forma linda e agradável - com imagens, descrições e o escambaul - na timeline".
{% highlight html %}
<meta itemprop="author" content="Perera">
<!-- Meu nome por que sou o autor dessa bagaça de artigo -->
{% endhighlight %}

Passamos da fase da teoria para dar aquela analisada básica nas tags que irei utilizar nesse blog. Se você der uma olhada no código html da página verá-lhe-lho-as no código.

## Quais meta tags utilizarei no blog?
**Charset**
Imprescindível! Muito pequeno gafanhoto se ferra pois o seu arquivo não está sendo lido corretamente devido ao charset. Essa tag fala pro browser qual o charset é utilizado por você.
{% highlight html %}
<meta charset="utf-8" />
<!-- Meu nome por que sou o autor dessa bagaça de artigo -->
{% endhighlight %}
**Keywords**
A keywords é um clássico que foi mal utilizado durante bom tempo e agora o google a desconsidera. O pessoal descobriu que era só colocar as palavras que todo mundo tava procurando para que seu site sofresse uma alavancagem nos resultados da busca. Hoje em dia os buscadores levam em consideração a coerência semântica, ou seja, se as palavras chaves estiverem coerente com o conteúdo da sua página ela é melhor rankeada.
{% highlight html %}
<meta name="keywords" content="html, meta tags, microdata, front-end, SEO,
HTML5, http, http-equiv, w3c">
<!-- Meu nome por que sou o autor dessa bagaça de artigo -->
{% endhighlight %}
**Viewport**
Como bem disse o Diego Eis do Tableless [nesse artigo](http://tableless.com.br/manipulando-metatag-viewport/), viewport é a área da tela onde seu website aparece. As definições do viewport são providenciais para que possamos controlar a visualização em vários tamanhos de tela. Caso queira saber mais leia o artigo do Diego que é duca.
{% highlight html %}
<meta name="viewport" content="width=device-width, initial-scale=1,
user-scalable=no">
{% endhighlight %}
**Description**
Essa meta dá uma descrição resumida da sua página. Utilizo normalmente a primeira frase do artigo pois é isso que aparece na descrição de um resultado no google, consequentemente minha primeira frase deve ter claramente o assunto tratado.
{% highlight html %}
<meta name="description" content="É isso mesmooo, temos nosso primeiro artigo,
e será sobre meta tags!! Mas por quê? Por que eu to indo criar as meta tags
desse blog agora, e após fuçar o blo..">
{% endhighlight %}
**Autor**
Nesse caso temos uma verdadeira assinatura dos créditos de quem escreveu a página.
{% highlight html %}
<meta name="author" content="Perera">
{% endhighlight %}
**Itemprop Author, name e description**
Coloquei essas metas juntas pois elas são exatamente a mesma coisa das metas com name description, author. E a de itemprop = name é relacionado a tag title. São informações duplicadas declaradas de forma diferente para abranger, por exemplo, o google plus.
{% highlight html %}
<meta itemprop="author" content="Perera">
<meta itemprop="name" content="O que são meta tags HTML e quais utilizarei
nesse blog?">
<meta itemprop="description" content="É isso mesmooo, temos nosso primeiro
artigo,e será sobre meta tags!! Mas por quê? Por que eu to indo criar as
meta tags desse blog agora,e após fuçar o blo..">
{% endhighlight %}
**Meta tags do facebook**
E pra finalizar, como exemplo gigantesco, segue as meta tags do open graph do facebook. A partir dessas declarações, ele define como publicar e mapear a sua página no facebook.
Acabou a cerveja, então não vou explicar uma a uma, pesquisa ae seu vagabundo.
{% highlight html %}
<meta property="fb:app_id" content="333451410072252" />
<meta property="og:locale" content="pt_BR" />
<meta property="og:type" content="article" />
<meta property="og:title" content="O que são meta tags HTML e quais utilizarei nesse blog?" />
<meta property="og:description" content="É isso mesmooo, temos nosso primeiro
artigo,e será sobre meta tags!! Mas por quê? Por que eu to indo criar as
meta tags desse blog agora,e após fuçar o blo.." />
<meta property="og:url" content="http://felipequadros.com/meta-tags/html/front-end/2016/05/15/meta-tags-do-blog/">
<meta property="og:site_name" content="Blog do Perera" />
<meta property="article:publisher" content="https://www.facebook.com/felipepereira.quadrosmaia" />
<meta property="article:author" content="https://www.facebook.com/felipepereira.quadrosmaia" />
<meta property="article:section" content="HTML" />
{% endhighlight %}

Agora que você já ta o bixão em meta tags, vai dar uma lida sobre a relação das meta tags e o SEO . A pessoa que não dá uma lida em SEO bom sujeito não é.

É o primeiro artigo e gostei demais do assunto, sempre ficava perdido com algumas metas. Nesse momento não tem plugin de comentários, mas entrem em contato comigo pelo [meu face](https://www.facebook.com/felipepereira.quadrosmaia) e vamos trocar ideia!!

Acho que o próximo será sobre o Jekyll que é o bixão demais. Abraços!
