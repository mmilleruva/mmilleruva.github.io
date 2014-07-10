---
layout: post
title:  "Getting Started With Chef"
date:   2014-07-09 23:08:03
categories: Chef Dev-Ops
---


So I started going through the the LearnChef guide and I wanted to put down some of my thoughts as I went through.

Basic Environment:

* Chef Server - This the hub for all configuration
* Nodes - The machines in your architecture (db servers, app servers, ...)
* Admin Console - Your machine, where you will enter commands


Basic tools:

* knife - The admin tool for performing a number of tasks
* chef-client - Installed on a node, this is how nodes communicate with chef


## Concepts

### Resources
resources are specifications about how a system should be configured:

Example:

{% highlight ruby %}
package "httpd" do
  action :install
end
{% endhighlight %}

This statement/resource specifies that the httpd package should be installed on the machine.

Here are some of the other common resources you may encounter:

* service - for controlling processes
* template - for controlling files

An **important** thing to note is resources
are **declarative**. This means the resource only specifies that the
httpd package should be installed. It does not specify how it should
be installed (i.e. with yum, apt-get). To actually know how to install
the package, Chef uses providers.

### Providers

Chef uses the platform to determine which provider should be used to
carryout the resource specification.


### Recipes
Recipes contain a list of resources.

Example:


{% highlight ruby%}
package "httpd" do
  action :install
end

package "sox" do
  action :install
end

service "httpd" do
  action [:enable, :start]
end

template "/var/www/html/index.html" do
  source "index.html.erb"
  mode "0644"
end

{% endhighlight ruby%}

### Run List
The ordered set of recipes and roles that the chef client will execute on a node.


