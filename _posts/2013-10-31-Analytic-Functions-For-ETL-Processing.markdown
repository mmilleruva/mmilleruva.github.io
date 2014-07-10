---
layout: post
title:  "Using Analytic Functions To Filter Bad Data During ETL Processing"
date:   2013-10-31 23:08:03
categories: Analytic Functions T-SQL
---

Filtering out bad records from a database can be a subtly tricky problem. One situation I have seen several times, is attempting to remove duplicate records from a table based on some business rule. For example, lets use the hypothetical situation where there is a Property table and a Property Manager Table. There is a business rule that each property should only have a single property manager. Looking at the dummy data I created below we can see that is not the case.


<table class="CSSTableGenerator">
    <tr>
      <td>Property ID</td>
      <td>Property Name</td>
    </tr>
    <tr>
      <td>1</td>
      <td>Building 1</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Building 2</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Building 3</td>
    </tr>
</table>

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll's GitHub repo][jekyll-gh].

[jekyll-gh]: https://github.com/jekyll/jekyll
[jekyll]:    http://jekyllrb.com
