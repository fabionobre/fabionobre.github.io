---
layout: post
title:  "Working with Lists - Java vs Rails"
date:   2016-06-30 11:34:00
categories: dicas
image: /assets/photos/dicas.jpg
---
Working with lists can be easy in certain languages and very difficult in others.

Java is a powerfull language used everywhere in all over the world. But Java is a very verbose language, to do something easy you have to write a lot of code. You have to make everything very explicity.

Ruby is a powerful language too, but is more focused on web applications because of the Rails framework. In Ruby, you do not have to write a lot of code. You can do something easy in a easy way. 

And that's what I will show in this post. I will show how to work with lists in these two languages and show the differences between them.

First example, I have to return another list only with even numbers contained in the first list.

{% highlight ruby %}
a = [1,2,3,4,5,6,7,8,9,10]
b = a.select {|n| n % 2 == 0}
{% endhighlight %}

{% highlight java %}
List<Integer> a = new ArrayList<Integer>(Arrays.asList(1,2,3,4,5,6,7,8,9,10));
List<Integer> b = new ArrayList<Integer>();

for (Integer elem : a) {
	
	if (elem % 2 == 0) {
		b.add(elem);
	}
}
{% endhighlight %}

Second example, I have to delete the odd numbers of my list.

{% highlight ruby %}
a = [1,2,3,4,5,6,7,8,9,10]
a.delete_if {|i| i % 2 != 0}
{% endhighlight %}

{% highlight java %}
List<Integer> a = new ArrayList<Integer>(Arrays.asList(1,2,3,4,5,6,7,8,9,10));

for (Iterator<Integer> elem = a.iterator(); elem.hasNext();) {
	
	if (elem.next() % 2 != 0) {
		elem.remove();
	}
}
{% endhighlight %}

I work with Java every day, and I know a lot of his verbosity and that's why I love Ruby.