# Harshal's Blog

A personal blog built with Jekyll, featuring posts about programming and technology.

## Overview

This is a Jekyll-powered blog that covers various topics including programming languages, software development, and technical tutorials. The blog is designed with a clean, responsive layout and includes features like categorized posts and an about page.

## Features

- **Responsive Design**: Mobile-friendly layout that works across all devices
- **Category-based Organization**: Posts are organized by categories (General, Programming)
- **Custom Styling**: SCSS-based styling with modular components
- **RSS Feed**: Automatic feed generation with jekyll-feed plugin
- **Easy Content Management**: Write posts in Markdown format

## Getting Started

### Prerequisites

- Ruby (version 2.7 or higher)
- Bundler gem
- Git

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/saturnyx/blog.git
   cd blog
   ```

2. Install dependencies:

   ```bash
   bundle install
   ```

3. Serve the site locally:

   ```bash
   bundle exec jekyll serve
   ```

4. Open your browser and visit `http://localhost:4000`

### Creating New Posts

You can create new posts using Jekyll Compose (already included in the Gemfile):

```bash
bundle exec jekyll post "Your Post Title"
```

Or manually create a new file in the `_posts` directory following the naming convention:
`YYYY-MM-DD-your-post-title.md`

## Project Structure

```text
├── _config.yml          # Site configuration
├── _includes/           # Reusable HTML components
│   ├── ad.html
│   ├── analytics.html
│   ├── footer.html
│   └── nav.html
├── _layouts/            # Page templates
│   ├── page.html
│   └── post.html
├── _posts/              # Blog posts
├── assets/
│   └── css/             # SCSS stylesheets
├── about.md             # About page
├── index.html           # Homepage
├── posts.html           # Posts listing page
└── 404.html            # Custom 404 page
```

## Configuration

The site configuration is managed in `_config.yml`. Key settings include:

- **Site Title**: Harshal's Blog
- **Author**: Harshal
- **Email**: `saturnyx@disroot.org`
- **GitHub**: saturnyx

## Styling

The blog uses SCSS for styling with the following structure:

- `main.scss` - Main stylesheet that imports all components
- `var.scss` - Variables and theme configuration
- `nav.scss` - Navigation styling
- `footer.scss` - Footer styling
- `post.scss` - Individual post styling
- `posts.scss` - Posts listing page styling
- `index.scss` - Homepage styling

## Deployment

This site can be deployed to various platforms:

### GitHub Pages

1. Push your code to a GitHub repository
2. Enable GitHub Pages in repository settings
3. Your site will be available at `https://username.github.io/repository-name`

### Netlify

1. Connect your GitHub repository to Netlify
2. Set build command: `bundle exec jekyll build`
3. Set publish directory: `_site`

### Manual Deployment

1. Run `bundle exec jekyll build`
2. Upload the contents of `_site` directory to your web server

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add new feature'`)
5. Push to the branch (`git push origin feature/new-feature`)
6. Create a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

## Contact

- **Author**: Harshal
- **Email**: `saturnyx@disroot.org`
- **GitHub**: [@saturnyx](https://github.com/saturnyx)

---

Built with ❤️ using [Jekyll](https://jekyllrb.com/)