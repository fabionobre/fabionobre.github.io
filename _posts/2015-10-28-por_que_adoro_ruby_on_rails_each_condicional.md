---
layout: post
title:  "Por que adoro Ruby on Rails - Each condicional"
date:   2015-10-28 22:00:00
categories: desenvolvimento
tags: featured
image: /assets/photos/desenvolvimento.jpg
---
Normalmente fazer uma iteração em uma lista são necessárias algumas linhas de codigo. E se você precisar filtrar a lista e exibir apenas alguns elementos dela, como fazer ?

Com Rails é algo simples e trivial. 

Digamos que você tenha uma lista de produtos e necessita exibir apenas os produtos ativo. Como fazer em rails ?

{% highlight ruby %}
produtos.where(:ativo => true).each do |produto|
  puts produto
end
{% endhighlight %}

Simplesmente simples e fantástico.