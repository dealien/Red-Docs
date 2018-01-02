# Documentation and Tutorials For [Red-Magician](https://github.com/dealien/Red-Magician)

[Open docs](https://dealien.github.io/Red-Docs/)

## Adding New Docs
In order to ensure uniformity within the documentation, you __MUST__ follow these steps when creating new docs. 

#### File Name
 * First of all, you need to create a new markdown (`.md`) file inside [`/red`](../tree/gh-pages/red) on the `gh-pages` branch.
   * The name of this new file should be `red_<category>_<topic>.md`.

#### Front Matter
 * Add a front matter header as follows:<a name="front-matter"></a>
```
  ---
  title: <your_title>
  sidebar: red_sidebar
  permalink: /red_<category>_<topic>/
  ---
```

#### Syntax
 * Write your doc in GitHub's markdown syntax. Note that there are a few of jekyll-oriented exceptions, that you have to keep in mind:
   * All the block elements (each line in a list, code blocks, titles, tables, and images) should be separated from everything before and after by newlines
   * Title should have one whitespace after `#` symbols. `### Like this`
   * Internal links should start with `/Red-Docs/` and have a trailing `/` like this: `[Example](/Red-Docs/example/)`

#### Categorization & The Sidebar
 * To add your doc to the sidebar, you need to add it to [`_data/sidebars/red_sidebar.yaml`](../blob/gh-pages/_data/sidebars/red_sidebar.yaml). 
   * Choose a category for your doc, or add a new one based off this template (indentation is important here):
```
- title: Overview
    output: web
    folderitems:
```
  * Add your doc using the following template:
```
- title: Installing on Linux
      url: /red_install_linux/
      output: web
```

Now all that's left to do is write the doc. 
