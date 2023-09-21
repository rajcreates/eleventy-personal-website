---
title: 'Building a Blog with Eleventy and Markdown - A Step-by-Step Tutorial'
description: "Creating a blog is a common use case for static site generators, and Eleventy makes it incredibly easy to do so. In this tutorial, we'll walk you through the process of building a simple blog using Eleventy and Markdown."
date: 2023-09-19
---

## Introduction

Creating a blog is a common use case for static site generators, and Eleventy makes it incredibly easy to do so. In this tutorial, we'll walk you through the process of building a simple blog using Eleventy and Markdown.

## Prerequisites

- Basic knowledge of HTML, CSS, and JavaScript
- Node.js and npm installed on your computer

## Step 1: Setting Up Your Project

1. Create a New Directory: Make a new directory for your blog and navigate into it.

2. Initialize npm: Run npm init -y to create a package.json file.

3. Install Eleventy: Run npm install --save-dev @11ty/eleventy.

## Step 2: Configuration

Create a .eleventy.js file in your project root. This file will hold your Eleventy configuration. For now, it can be empty.

## Step 3: Creating Blog Posts

1. Create a posts directory in your project root.

2. Inside posts, create Markdown files for your blog posts, e.g., my-first-post\.md.

## Step 4: Front Matter

In each Markdown file, add front matter to specify metadata like the title and date:

```markdown
---
title: "My First Post"
date: 2023-09-20
---
```

## Step 5: Writing Content

Below the front matter, write your blog post content in Markdown format.

## Step 6: Creating a Blog List Page

Create an index.njk file in your project root and use Nunjucks templating to list your blog posts:


```nunjucks
{% raw %}
{% for post in collections.posts %}
  <article>
    <h2>{{ post.data.title }}</h2>
    <p>{{ post.date | date: "%B %d, %Y" }}</p>
  </article>
{% endfor %}
{% endraw %}
```

## Step 7: Styling

Add a styles.css file to style your blog. Link it in your index.njk file.

## Step 8: Building the Blog

Run npx eleventy to build your blog. The output will be in the _site directory.

## Step 9: Deployment

Deploy your blog to a hosting service of your choice, such as Netlify or Vercel.

## Conclusion

Building a blog with Eleventy and Markdown is a straightforward process that offers a lot of flexibility. You can easily extend this basic setup with additional features like tags, categories, and pagination.