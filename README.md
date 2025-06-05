# My Hugo Blog with ox-hugo

This is a Hugo-based blog that uses the Blowfish theme and is configured to work with Emacs org-mode and ox-hugo.

## Prerequisites

1. [Hugo](https://gohugo.io/installation/)
2. [Emacs](https://www.gnu.org/software/emacs/)
3. [ox-hugo](https://ox-hugo.scripter.co/)

## Setup

1. Clone this repository:
   ```bash
   git clone <your-repo-url>
   cd myblog
   git submodule update --init --recursive
   ```

2. Install ox-hugo in Emacs:
   ```elisp
   (use-package ox-hugo
     :ensure t
     :after ox)
   ```

## Directory Structure

- `org/content/posts/` - Your org-mode blog posts
- `content/` - Generated Hugo content (do not edit directly)
- `themes/blowfish/` - The Blowfish theme

## Writing Posts

1. Create a new org file in `org/content/posts/`
2. Add the necessary ox-hugo export settings at the top of your org file:
   ```org
   #+title: Your Post Title
   #+date: YYYY-MM-DD
   #+author: Your Name
   #+tags: [tag1, tag2]
   #+categories: [category1]
   #+hugo_base_dir: ../../
   #+hugo_section: posts
   #+hugo_draft: false
   ```

3. Write your post in org-mode
4. Export to Hugo markdown using `C-c C-e H H` in Emacs

## Preview

To preview your blog locally:

```bash
hugo server -D
```

Visit `http://localhost:1313` in your browser.

## Building

To build the static site:

```bash
hugo
```

The generated site will be in the `public/` directory.

## Customization

- Edit `hugo.toml` to modify site configuration
- Customize the Blowfish theme settings in `hugo.toml`
- Add your own CSS in `assets/css/custom.css`

## License

This project is licensed under the MIT License - see the LICENSE file for details. 