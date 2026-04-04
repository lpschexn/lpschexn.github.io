# lpschexn.github.io

Personal academic website for Logan Schexnaydre.

## Editing homepage content

Almost everything visible on the homepage is controlled by a single file:

**`_data/content.yml`**

Edit that file, commit, and push — GitHub Pages rebuilds automatically (usually within ~1 minute).

### Hero (name, title, institution)

```yaml
hero:
  name: "Logan Schexnaydre"
  pronouns: "(he/him)"
  title: "PhD Candidate"
  keywords: "Stochastic Modeling &middot; Autonomous Sensing &middot; Sustainable Computing"
  institution: "Michigan Technological University"
  department: "Dept. of Electrical &amp; Computer Engineering"
  graduation: "Graduating Summer 2026"
  email: "lpschexn@mtu.edu"
```

`keywords` appears as plain text below the title and above the institution line.  
Use `&middot;` for the dot separator ( · ).

### Gallery (photo carousel)

```yaml
gallery:
  photos:
    - src: "images/my-photo.jpg"
      alt: "Description for screen readers"
      caption: "Optional caption shown on the photo"   # omit to hide
      link: "https://example.com"                      # omit for no link
```

Place images in the `images/` folder. Add or remove items freely — the carousel appears only when at least one photo is listed.

### Research section

```yaml
research:
  heading: "What I Work On"
  paragraphs:
    - >-
      First paragraph text...
    - >-
      Second paragraph text...
  keywords:
    - "Lidar Processing"
    - "Autonomous Vehicles"
```

Add or remove paragraphs and keywords freely.

### Publications (Selected Works)

```yaml
publications:
  heading: "Selected Works"
  scholar_url: "https://scholar.google.com/..."   # omit to hide the footer link
  items:
    - title: "Paper title"
      authors: "<strong>L. Schexnaydre</strong>, A. Coauthor"
      venue: "Journal or conference name"
      year: 2025
      link: "https://doi.org/..."
      badges:           # optional
        - first         # renders blue "First Author" pill
        - preprint      # renders plain pill with that text
```

Wrap your own name in `<strong>...</strong>` to bold it in the author list.

### Projects

```yaml
projects:
  heading: "Research &amp; Initiatives"
  items:
    - name: "Project name"
      image: "images/my-image.jpg"    # optional
      image_alt: "Alt text"           # optional, defaults to project name
      desc: >-
        Description text.
      link: "https://example.com"
      link_text: "Visit project"
```

Omit `image` to show a generic placeholder. Add or remove items freely.

### Research Vision

```yaml
vision:
  heading: "Research Vision"
  paragraphs:
    - >-
      Paragraph text...
  tags:
    - "Postdoctoral positions"
```

### Contact tagline

```yaml
contact:
  tagline: >-
    Short message shown above the email button.
```

### Footer

```yaml
footer:
  copyright: "&copy; 2026 Logan Schexnaydre"
```

---

### Adding images

Drop image files into the `images/` folder, then reference them as `"images/filename.jpg"` in `content.yml`.

### Running locally

If `bundle` is not found, install bundler first:

```bash
gem install bundler
```

You may also need to add the gem bin directory to your PATH (the `gem install` output will show the path if so):

```bash
export PATH="$HOME/.local/share/gem/ruby/3.4.0/bin:$PATH"
```

Then install dependencies and start the server:

```bash
bundle install
bundle exec jekyll serve -l -H localhost
```

Site serves at `http://localhost:4000`. Live-reloads on file changes (except `_config.yml`).

---

# Academic Pages
**Academic Pages is a GitHub Pages template for personal and professional portfolio-oriented websites.**

![Academic Pages template example](images/homepage.png "Academic Pages template example")

# Getting Started

1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Click the "Use this template" button in the top right.
1. On the "New repository" page, enter your repository name as "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and add your content.
1. Upload any files (like PDFs, .zip files, etc.) to the `files/` directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.
1. Check status by going to the repository settings, in the "GitHub pages" section
1. (Optional) Use the Jupyter notebooks or python scripts in the `markdown_generator` folder to generate markdown files for publications and talks from a TSV file.

See more info at https://academicpages.github.io/

## Running locally

When you are initially working your website, it is very useful to be able to preview the changes locally before pushing them to GitHub. To work locally you will need to:

1. Clone the repository and made updates as detailed above.
1. Make sure you have ruby-dev, bundler, and nodejs installed
    
    On most Linux distribution and [Windows Subsystem Linux](https://learn.microsoft.com/en-us/windows/wsl/about) the command is:
    ```bash
    sudo apt install ruby-dev ruby-bundler nodejs
    ```
    If you see error `Unable to locate package ruby-bundler`, `Unable to locate package nodejs `, run the following:
    ```bash
    sudo apt update && sudo apt upgrade -y
    ```
    then try run `sudo apt install ruby-dev ruby-bundler nodejs` again.

    On MacOS the commands are:
    ```bash
    brew install ruby
    brew install node
    gem install bundler
    ```
1. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.

    If you see file permission error like `Fetching bundler-2.6.3.gem ERROR:  While executing gem (Gem::FilePermissionError) You don't have write permissions for the /var/lib/gems/3.2.0 directory.` or `Bundler::PermissionError: There was an error while trying to write to /usr/local/bin.`
    Install Gems Locally (Recommended):
    ```bash
    bundle config set --local path 'vendor/bundle'
    ```
    then try run `bundle install` again. If succeeded, you should see a folder called `vendor` and open `.gitignore` then add `vendor` inside it.

1. Run `jekyll serve -l -H localhost` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change.
    You may also try `bundle exec jekyll serve -l -H localhost` to ensure jekyll to use specific dependencies on your own local machine.

If you are running on Linux it may be necessary to install some additional dependencies prior to being able to run locally: `sudo apt install build-essential gcc make`
---
<div align="center">
    
![pages-build-deployment](https://github.com/academicpages/academicpages.github.io/actions/workflows/pages/pages-build-deployment/badge.svg)
[![GitHub contributors](https://img.shields.io/github/contributors/academicpages/academicpages.github.io.svg)](https://github.com/academicpages/academicpages.github.io/graphs/contributors)
[![GitHub release](https://img.shields.io/github/v/release/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io/releases/latest)
[![GitHub license](https://img.shields.io/github/license/academicpages/academicpages.github.io?color=blue)](https://github.com/academicpages/academicpages.github.io/blob/master/LICENSE)

[![GitHub stars](https://img.shields.io/github/stars/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io)
[![GitHub forks](https://img.shields.io/github/forks/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io/fork)
</div>
