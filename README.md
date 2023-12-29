# Post Viewer Documentation

## Overview

The Post Viewer is a flexible JavaScript-based solution designed to display posts from JSON files on an HTML webpage. It supports multiple containers, each with its own settings, allowing you to showcase different sets of posts with various configurations.

## Usage

### HTML Structure

Include the necessary HTML structure in your webpage. For each post container, use the following format:

```html
<div class="post-container"
     data-json-url="path/to/your/posts.json"
     data-order="natural|random"
     data-max-results="number">
</div>
```

- **data-json-url:** Specifies the path to the JSON file containing post data.
- **data-order:** Defines the order of post display. Use "natural" for the default order and "random" for a random order.
- **data-max-results:** Sets the maximum number of posts to display.

### Script

Ensure the following script is included in your HTML file:

```html
<script>
  // Fetch data from each JSON file and display posts
  document.querySelectorAll('.post-container').forEach(container => {
    // ... (script details)
  });
</script>
```

## Configuration Options

### JSON File

Create a JSON file (e.g., posts.json) with an array of post objects. Each post can have the following optional fields:

- **title:** Post title.
- **description:** Post description.
- **date:** Date of publication or update.
- **image:** URL of the post image.
- **url:** URL of the full post.
- **author:** Post author.
- **categories:** Array of post categories.

### Attributes

- **data-json-url:** Path to the JSON file.
- **data-order:** "natural" for default order, "random" for random order.
- **data-max-results:** Maximum number of posts to display.

## Example

```html
<div class="post-container"
     data-json-url="posts.json"
     data-order="random"
     data-max-results="5">
</div>
```

This example fetches data from `posts.json`, displays posts in a random order, and shows a maximum of 5 posts.
