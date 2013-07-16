---
layout: post
title: My first blog post
categories: first
---

This is my first blog post.

{% highlight ruby %}
require 'json'

def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end

class User < ActiveRecord::Base
  validates :login, :name, presence: true
end
{% endhighlight %}


