---
title: 'Creating Dynamic Content with Eleventy and Headless CMS'
description: "Static site generators like Eleventy are excellent for creating fast and secure websites, but what if you need to manage dynamic content? This is where a Headless CMS comes into play. In this blog post, we'll explore how to integrate Eleventy with a Headless CMS to create a dynamic, yet performant, website."
date: 2023-09-18
---

## Introduction

Static site generators like Eleventy are excellent for creating fast and secure websites, but what if you need to manage dynamic content? This is where a Headless CMS comes into play. In this blog post, we'll explore how to integrate Eleventy with a Headless CMS to create a dynamic, yet performant, website.

## What is a Headless CMS?

A Headless Content Management System (CMS) is a back-end-only content management system that provides an API for delivering content. Unlike traditional CMSs, it doesn't come with a front-end layer, giving you the freedom to use any front-end technology you like—such as Eleventy.

## Why Use a Headless CMS with Eleventy?

- Content Flexibility: Easily manage and update content without touching the code.
- Developer Experience: Use your preferred front-end technologies and frameworks.
- Scalability: As your content grows, a Headless CMS can easily adapt.

## Popular Headless CMS Options

- Contentful
- Strapi
- Sanity
- Ghost

## Setting Up the Integration

1. Choose a Headless CMS: Pick a CMS that suits your needs and set up an account.

2. Create Content Models: Define the types of content you'll be managing.

3. Add Content: Populate your CMS with the actual content you want to display.

4. Fetch Content: Use the CMS's API to fetch content into your Eleventy project.

## Fetching Content in Eleventy

Here's a simple example using JavaScript to fetch content from a Headless CMS:

```javascript
const fetch = require("node-fetch");

module.exports = async function() {
  const res = await fetch("https://your-cms-api.com/posts");
  const posts = await res.json();
  return posts;
};
```

## Displaying Dynamic Content

Once you've fetched the content, you can use Eleventy's templating to display it:

```nunjucks
{% raw %}
{% for post in posts %}
  <article>
    <h2>{{ post.title }}</h2>
    <p>{{ post.content }}</p>
  </article>
{% endfor %}
{% endraw %}
```

## Conclusion

Integrating a Headless CMS with Eleventy allows you to manage dynamic content easily while still benefiting from the performance and security of static sites. This combination offers a powerful, flexible solution for modern web development.