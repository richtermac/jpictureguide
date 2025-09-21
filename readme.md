# jpicture.net guide

## Add or change top navigation menu items

- Where: `hugo.toml`

```toml
[menu]

[[menu.main]]
name = "Home"
url = "/"
weight = 10

[[menu.main]]
name = "Professionals"
url = "/professionals/"
weight = 20
```

- Weights control order (smaller shows first).

## Add new anchor sections and link to them

1. Add an id to any section you want to link to:

Example: 
id: "new-section"

```yaml
####################### Banner #########################
style: "style5 invert orient-left content-align-center image-position-center"
title: "New Section"
id: "new-section"
subtitle: |
  Optional subtitle
content: |
  Body copy with <a href="#artwork">internal anchor</a>.
button:
  label: "Learn more"
  link: "/new-page"
image: "images/example.jpg"
```

2. Link to it from anywhere (including other data content) using `href="#new-section"`.

### Your existing examples:

- Anchor links in banner content:

```/data/banner.yml
I specialise in photographing <a href="#portraits">people</a> and <a href="#artwork">artwork</a>;
...
label: "Get Started"
link: "#portraits"
```

- Section IDs defined in data:

```/data/spotlight_banner_portraits.yml
title: "Portraits"
id: "portraits"
```

### Edit email, phone number, and Pixelfed

- Where: `hugo.toml` → `[Params.social]`

```hugo.toml
[Params.social]
email = "sayhello@jpicture.net"
phone = "+1234567890"
pixelfed = "https://pixelfed.social/Eliptic"
```

- Tips:
  - Keep `phone` in a tel-friendly format (e.g., `+441234567890`).
  - `mailto:` and `tel:` are generated automatically from these values.
