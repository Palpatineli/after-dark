# breeze

## Contents

- [Installation](#installation)
- [Options](#options)
  - [Top menu](#top-menu)
  - [Title](#title)

## Installation
First download this theme to your `themes` directory:

```bash
$ cd themes
$ git clone https://github.com/Palpatineli/breeze-theme.git
```
and then enable it in your `config.toml`:

```toml
theme = "breeze"
```

The posts should be in directly under the `content` folder.

The theme requires tags and categories taxonomies to be enabled in your `config.toml`:

```toml
taxonomies = [
    # You can enable/disable RSS
    {name = "categories", rss = true},
    {name = "tags", rss = true},
]
```
If you want to paginate taxonomies pages, you will need to overwrite the templates
as it only works for non-paginated taxonomies by default.


## Options

### Top-menu
Set a field in `extra` with a key of `after_dark_menu`:

```toml
menu = [
    {url = "$BASE_URL", name = "Home"},
    {url = "$BASE_URL/categories", name = "Categories"},
    {url = "$BASE_URL/tags", name = "Tags"},
    {url = "https://google.com", name = "Google"},
]
```

If you put `$BASE_URL` in a url, it will automatically be replaced by the actual
site URL.

### Title
The site title is shown on the homepage.

### Network
Optionally network icons and links can be added in config

Currently github, linkedin, and research gate are supported

```toml
[extra.network]
"github" = "https://github.com/Palpatineli"
"linkedin" = "https://www.linkedin.com/in/keji-li-64080620/"
"researchgate" = "https://www.researchgate.net/profile/Keji_Li2"
```

## Original
This template is based on the after-dark template by Keats himself https://github.com/Keats/after-dark.git
