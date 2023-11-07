# GovLike theme for Jekyll

## About this theme

This is a simple theme for [Jekyll](https://www.jekyllrb.com) based on the [GOV.UK Design System](https://design-system.service.gov.uk), for use as a simple blog. It takes the Sass files from the design system, and select HTML components to give a similar look to GOV.UK, but without GOV.UK specific design flourishs like the Crown symbol or Royal crest.

## Using the theme

### Installation

To use this theme on your Jekyll build, include the `jekyll-remote-theme` plugin and add the following to your configuration file:

```
# Jekyll build settings
remote_theme: johnpeart/govlike
```

### Pagination

This theme requires the `jekyll-paginate` plugin.

### Set up the site

You can control the site header, footer and sidebar through settings in the site `_config.yml` file.

#### Site header

The following settings are available and can be set using nested YAML markup:

```
header:
  type: "default" # Set to "default", "service-name" or "service-name-with-navigation" to change the header
  site-name: "GovLike" # Appears in the header, regardless of style
  service-name: "Service name" # Appears in the header, if site.header.type is set to "service-name" or "service-name-with-navigation"
  # links:
  # - name: "Item 1"
  #   url: "/"
  #   alt: "Go to Item 1"
  # - name: "Item 2"
  #   url: "/2/"
  #   alt: "Go to Item 2"
```


#### Site footer

The following settings are available and can be set using nested YAML markup:

```
footer:
  type: "default" # Set to "default"
  ogl: false # Display (true) or disable (false) the OGL licence text
  crown-copyright: false # Display (true) or disable (false) the Crown copyright text and symbol
  # links:
  # - name: "Item 1"
  #   url: "/"
  #   alt: "Go to Item 1"
  # - name: "Item 2"
  #   url: "/2/"
  #   alt: "Go to Item 2"
```

#### Site header

The following settings are available and can be set using nested YAML markup:

```
sidebar:
  type: "default" # Set to "default"
  description: "A basic Jekyll theme built on the GOV.UK Design System"
```

By default, the sidebar will take the text set in `site.description` and set it in the sidebar, if a separate description is not set here..

### Adding posts and pages

To create the blogroll, create an `index.html` file. In the front matter, include:

```
---
layout: home
---
```

You can add posts by adding them to the `_posts` folder, and pages to the `_pages` folder. Posts and pages require YAML front matter to correctly display.

Header images can be set using nested YAML under the `image` tag. Setting an image source or caption will wrap the image in a `<figure>` tag, and place the text in a `<figcaption>` tag. Otherwise, the image will be set as a plain `img` tag.

```
---
title: 'Another sample post: so you can see how multiple posts work'
excerpt: 'This is a second sample post. We've created this to demonstrate how the templates work.'
image:
  url: '/assets/images/govuk-opengraph-image.png'
  source: 'Name of source'
  alt: 'Descriptive text for a header image'
  caption: 'A caption for this image.'
author: 'GovLike'
---
```

### Writing posts

Posts should be written in Markdown.

```
# Heading Level 1

## Heading Level 2

### Heading Level 3

Paragraph text

[Links](//www.example.com "Title text for the link")

<mailtoemailaddresses@example.com>

> Blockquote text

- unordered list item 1
- unordered list item 2
- unordered list item 3

1. ordered list item 1
2. ordered list item 2
3. ordered list item 3

Adding images

![alt text](/assets/image.png "Alt text for the image")

## Licence

The [license for the codebase](https://github.com/alphagov/govuk-frontend#licence) for the GOV.UK Design System is released under the MIT License. This covers both the codebase and any sample code in the documentation.
