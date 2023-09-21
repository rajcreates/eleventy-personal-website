---
title: 'Mastering Templating in Eleventy: Nunjucks, Liquid, and Beyond'
description: "One of Eleventy's most powerful features is its support for multiple templating languages. Whether you're a fan of Nunjucks, Liquid, or even plain old Markdown, Eleventy has you covered. In this blog post, we'll delve into the world of templating in Eleventy, exploring how you can leverage different engines for various use-cases."
date: 2023-09-20
---

## Introduction

One of Eleventy's most powerful features is its support for multiple templating languages. Whether you're a fan of Nunjucks, Liquid, or even plain old Markdown, Eleventy has you covered. In this blog post, we'll delve into the world of templating in Eleventy, exploring how you can leverage different engines for various use-cases.

## What Are Templating Engines?

Templating engines allow you to generate HTML dynamically. They provide a way to separate your website's logic from its layout, making it easier to manage and extend.

## Supported Templating Engines in Eleventy

Eleventy supports a wide range of templating engines, including:

- Nunjucks
- Liquid
- Handlebars
- EJS
- Markdown
- HTML

## Nunjucks: The Flexible Choice

Nunjucks is a rich and flexible templating engine with a syntax similar to Jinja2. It's great for complex layouts and offers features like template inheritance and custom filters.

#### Example: Using Nunjucks for Layouts

```nunjucks
{% raw %}
{% extends "base.njk" %}

{% block content %}
  <h1>{{ title }}</h1>
  <p>{{ content }}</p>
{% endblock %}
{% endraw %}
```

## Liquid: The Jekyll Standard

Liquid is the default templating engine for Jekyll, and it's a solid choice for those migrating from Jekyll to Eleventy.

#### Example: Using Liquid for Loops

```liquid
{% raw %}
{% for post in posts %}
  <h2>{{ post.title }}</h2>
  <p>{{ post.summary }}</p>
{% endfor %}
{% endraw %}
```

## Markdown: The Simplest Option

Markdown isn't technically a templating engine, but Eleventy allows you to use it as one. It's perfect for content-heavy pages like blog posts.

#### Example: Using Markdown for Content

```markdown
---
title: My Blog Post
---

# {{ title }}

Welcome to my blog post.
```

## Mixing and Matching

One of the best things about Eleventy is that you can use multiple templating engines in the same project. For example, you could use Nunjucks for your site layout, Liquid for a specific component, and Markdown for your blog posts.

## Conclusion

Mastering templating in Eleventy opens up a world of possibilities for your projects. Whether you're building a simple blog or a complex web application, understanding how to leverage different templating engines can make your development process more efficient and enjoyable.