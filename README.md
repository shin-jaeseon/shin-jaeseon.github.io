# Xaml Design Studio Website

This repository is for the [Xaml Design Studio](https://www.xamldesign.studio) website, hosted using GitHub Pages.

## Running the Site Locally

This site is built with Jekyll. To run it locally, follow these steps:

1. Install Ruby (https://www.ruby-lang.org/en/downloads/)
2. Install Jekyll and Bundler:
   ```
   gem install jekyll bundler
   ```
3. Clone the repository and navigate to its directory:
   ```
   git clone https://github.com/shin-jaeseon/shin-jaeseon.github.io.git
   cd shin-jaeseon.github.io
   ```
4. Install dependencies:
   ```
   bundle install
   ```
5. Run local server:
   ```
   bundle exec jekyll serve
   ```
6. Access in browser at `http://localhost:4000`

## Site Structure

- `_posts/`: Blog posts
- `_projects/`: Project information
- `assets/`: Static files such as images, CSS
- `_layouts/`: Layout templates
- `_includes/`: Reusable HTML components

## Adding Content

### Adding Blog Posts

Create a markdown file in the `_posts` directory with the format `YYYY-MM-DD-title.md` and add the following YAML front matter:

```yaml
---
layout: post
title: "Post Title"
date: YYYY-MM-DD
categories: category_name
tags: tag1 tag2
---
```

Then write your content in markdown.

### Adding Projects

Create a new markdown file in the `projects` directory.

## License

[Enter content: License information]
