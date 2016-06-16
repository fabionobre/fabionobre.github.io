---
layout: post
title:  "Why I love Ruby on Rails - Each condicional"
date:   2015-10-28 22:00:00
categories: desenvolvimento
image: /assets/photos/desenvolvimento.jpg
---
Usually iterating a list requires a lot of line of code. And if you want to filter the list to show only certain elements ? What will you do ?

Using rails is very simple.

Let's think that you have a list of products and have to filter and display only the actives. How do we do this in rails ?

{% highlight ruby %}
products.where(:active => true).each do |product|
  puts product
end
{% endhighlight %}

Really simple and fantastic.