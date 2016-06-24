---
layout: post
autor: felipeQuadros
title: 'Tipagem Fraca, Forte, Estática, Dinâmica e Inferência de Tipo'
categories: programação básico iniciante geral teoria
keywords: programação tipagem fraca forte estática dinâmica inferência-de-tipo linguagem
date: '2016-06-05 15:00:00 -0300'
section: Programação Iniciante
cervejaDoDia: Brahma Mega Latão
linkCerveja: >-
  http://distribuidoraourofino.com.br/products.php?product=cerveja-brahma-mega-lat%E3o-%252d-550ml-%252d-cx-24-unidades
---

Nas últimas semanas tenho descoberto que existe um débito técnico muito grande em relação a programação.

**Débito técnico: leia-se uma forma bonita que aprendi a falar para mostrar que tenho uma grande capacidade de programar sem saber de fato a aplicação, teoria, filosofia daquilo que está sendo escrito.**


**Tipagem fraca, forte, dinâmica, estática e inferência de tipos são 5 conceitos diferentes** - só pra ficar bem claro.

# Inferência de Tipo

A inferência de tipos é a capacidade do compilador entender/'adivinhar' qual é o tipo de dados de determinada variável sem ela ter sido declarada no código escrito. Isso, mastigue o conceito com calma tomando a sua cerveja.

Vamos aos exemplos. No C# temos inferência de tipo ao declarar variáveis locais com o "var" antes do nome da nossa variável, tipo:

{% highlight c# %}
var inferencia = 10; //Nossa variável 'inferencia' terá seu tipo setado em tempo de compilação
{% endhighlight %}

A lá, que beleza. Não declaramos tipo nenhum, mas na hora que o compilador enxerga o valor ele entende que é uma variável do tipo int, e é essa capacidade que define que uma linguagem **infere tipos**. Temos PHP, Python , Javascript, etc. Um exemplo contrário seria o Java, nela o tipo deve ser determinado na declaração da variável (Pelo que pesquisei está tendo um esforço gradual em colocar a inferência de tipo no java há algum tempo ver [JEP 286: Local-Variable Type Inferecen](http://openjdk.java.net/jeps/286) ).

# Tipagem Forte e Fraca

Uma forma simples de definir a tipagem forte e fraca é que, caso ela seja forte, teremos a verificação de tipos em todas as operações em tempo de execução ou compilação, já a fraca não temos essa verificação.

Por exemplo, temos nosso amigo Javascript que é uma tipagem fraca, ou seja, além de não ter a capacidade de detectar erros em operações de tipos diferentes, ela nos dá um resultado nas operações de tipos diferentes, mas como assim?

Em Javascript podemos fazer:

{% highlight Javascript %}

'1' + 1 // o resultado será '11'
'1' + true // o resultado será 1true

{% endhighlight %}

Abra seu navegador e teste amiguinho. O PHP é uma outra linguagem de tipagem fraca.

Um Exemplo de tipagem forte seria o Python. Fazendo as mesmas operações do Javascript no python temos:

{% highlight Python %}
'1' + 1
Traceback (most recent call last): File "
<stdin>", line 1, in <module>
TypeError: cannot concatenate 'str' and 'int' objects</module></stdin>

'1' + True
Traceback (most recent call last): File "
<stdin>", line 1, in <module>
TypeError: cannot concatenate 'str' and 'bool' objects</module></stdin>

{% endhighlight %}

**Note que PHP tem tipagem fraca e o Python tem tipagem forte mas as duas linguagens tem Inferência de Tipos.**

# Tipagem Estática e Dinâmica

Tipagem Estática é a capacidade de uma linguagem ajudar na segurança de tipos, onde, a partir do momento que uma linguagem determina o tipo de uma variável esse tipo não pode ser alterado durante a compilação, fazendo com que o jovem programador não se preocupe tanto pois o compilador acusará erro caso seja alterado o tipo de uma variável.

Por exemplo, em C#:

{% highlight C# %}
var i = 1; //Note que terá a inferência do tipo inteiro
i = 'A'; //Dará erro de compilação pois o tipo da variável é inteiro
{% endhighlight %}

Já na Tipagem Dinâmica temos a possibilidade de alterar o tipo da nossa variável em tempo de execução. A essa capacidade definimos uma linguagem como Dinâmica, como por exemplo, o nosso velho amigo Javascript, veja:

{% highlight Javascript %}

var i = 1; //Note que terá a inferência do tipo inteiro
i = 'A'; //A partir desse momento sua variável é do tipo string com o valor 'A'. Lance normal, segue o jogo.

{% endhighlight %}

**Note que o C# tem inferência de tipo, é forte e é estática, já o javascript tem inferência de tipo, é fraca e é dinâmica.**

Veja que uma linguagem com tipagem dinâmica, não implica em uma linguagem dinâmica, e em relação a isso já deixo o [post do akita](http://www.akitaonrails.com/2008/02/22/tradu-o-tipagem-din-mica-vs-linguagem-din-mica-explicado) que é uma tradução do post de Steven Devijver que analisa um terceiro post! :)

Um outro objetivo do blog é repassar conceito que deveriam ser básicos, mas pelo menos na minha cidade, a maioria das pessaos que conversam já vão direto pra um framework e passam batidos nesse tipo de diferença, o que acaba influenciando na qualidade dos profissionais, acredito eu.

Eae, vocês sabiam essas diferenças? Eu duvido!
