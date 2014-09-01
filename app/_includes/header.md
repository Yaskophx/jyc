<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
        <title>{{ page.title }}</title>
        <meta name="viewport" content="width=device-width">
        <link rel="canonical" href="{{ page.url }}" />
        <!-- build:css({app,.tmp}) /css/main.css -->
        <!-- Custom CSS -->
        <link rel="stylesheet" href="/css/main.css">
        <!-- endbuild -->
    </head>
    <body>
        
        <div class="site">
            <div class="header">
                <h1 class="title"><a href="/">{{ site.name }}</a></h1>
            {% capture location %}{{ page.url | remove_first:'/' | split:'/' | first }}{% endcapture %}
            <nav><ul>
                <li><a {% if location == 'about' %}class="active" {% endif %}href="/about/">About</a></li>
                <li><a {% if location == 'blog' %}class="active" {% endif %}href="/blog/">Blog</a></li>
                <li><a {% if location == 'contact' %}class="active" {% endif %}href="/contact/">Contact</a></li>
            </ul></nav>
        </div>