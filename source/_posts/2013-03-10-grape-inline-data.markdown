---
layout: post
title: "Grape API formatter for sending inline data."
date: 2013-03-10 21:14:48 -0500
comments: true
categories: rails ruby grape snippets
---

I needed to add a .png formatter to the [quandl](http://quandl.com/help/api) Grape API.

The png is generated using phantomjs, so it needed to be sent down inline.

```ruby
content_type :png, "image/png"
 
formatter :png, lambda { |response, env|
    path = response.try(:object).try(:to_png)
    rack = Rack::Response.new(File.read(path) , 200, { "Content-type" => "image/png" }).finish
    rack[2].body[0]
}
```