# Data Engineering Blog

A clean, fast, opinionated personal website using GitHub Pages and Jekyll that acts as a **data engineering brand hub**.

## Features

- **Professional Design**: Clean, minimal, modern UI with responsive design
- **Opinionated Content**: Strong takes on data engineering trends and practices
- **Fast Performance**: Static site generation with GitHub Pages
- **SEO Optimized**: Built-in SEO tags and structured data
- **Mobile Responsive**: Works perfectly on all devices

## Project Structure

```
/
├── _config.yml              # Jekyll configuration
├── index.md                 # Home page (positioning focused)
├── blog.md                  # Blog listing page
├── series.md                # Content series organization
├── about.md                 # About page
├── projects.md              # Projects showcase
├── _posts/                  # Blog posts
│   ├── 2024-01-15-stop-overusing-spark.md
│   ├── 2024-01-20-your-data-lake-is-probably-a-swamp.md
│   └── ... (more posts)
├── _layouts/                # Jekyll layouts
│   ├── default.html
│   └── post.html
├── _includes/               # Reusable components
│   ├── head.html
│   ├── navigation.html
│   └── footer.html
└── assets/
    └── css/
        └── style.css        # Custom styling
```

## Tech Stack

- **GitHub Pages**: Hosting and deployment
- **Jekyll**: Static site generator
- **Markdown**: Content authoring
- **CSS**: Custom styling (no frameworks)
- **No backend**: Pure static site

## Deployment

### Option 1: GitHub Pages (Recommended)

1. **Fork or clone this repository**
   ```bash
   git clone https://github.com/eerla/data-engineering-blog.git
   cd data-engineering-blog
   ```

2. **Update configuration**
   - Edit `_config.yml` with your details
   - `baseurl` is already set to "/data-engineering-blog" for project repository
   - Update `url` if needed

3. **Add your content**
   - Replace placeholder content in `_posts/` with your Medium articles
   - Update pages with your information

4. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

5. **Enable GitHub Pages**
   - Go to repository settings
   - Scroll to "GitHub Pages"
   - Select "Deploy from a branch" → "main" → "/ (root)"
   - Save and wait for deployment
   - Your site will be available at: https://eerla.github.io/data-engineering-blog/

### Option 2: Local Development

1. **Install Jekyll**
   ```bash
   gem install jekyll bundler
   ```

2. **Install dependencies**
   ```bash
   bundle install
   ```

3. **Run locally**
   ```bash
   bundle exec jekyll serve
   ```

4. **Visit site**
   Open `http://localhost:4000` in your browser

## Adding Content

### Blog Posts

1. Create new files in `_posts/` with format: `YYYY-MM-DD-title.md`
2. Add frontmatter:
   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   date: 2024-01-15
   categories: data-engineering
   tags: [tag1, tag2, tag3]
   ---
   ```

3. Add your content below the frontmatter

### Pages

Edit existing pages in the root directory:
- `index.md` - Homepage content
- `about.md` - About page
- `projects.md` - Projects showcase
- `blog.md` - Blog listing (auto-generated)
- `series.md` - Content series organization

## Customization

### Colors and Typography

Edit `assets/css/style.css` and modify the CSS custom properties at the top:

```css
:root {
  --primary-color: #1e3a8a;
  --primary-light: #3b82f6;
  --text-color: #1e293b;
  /* ... more variables */
}
```

### Navigation

Update `navigation` array in `_config.yml`:

```yaml
navigation:
  - title: "Home"
    url: "/"
  - title: "Blog"
    url: "/blog/"
  # Add more items as needed
```

### Social Links

Update `social.links` in `_config.yml`:

```yaml
social:
  name: Your Name
  links:
    - https://github.com/yourusername
    - https://medium.com/@yourusername
    - https://www.linkedin.com/in/yourprofile/
```

## SEO Features

- Automatic sitemap generation
- Meta tags for social sharing
- Structured data for search engines
- Clean URLs and permalinks
- Mobile-friendly design

## Analytics

1. **Google Analytics**: Add your tracking ID to `_config.yml`
   ```yaml
   google_analytics: GA_MEASUREMENT_ID
   ```

2. **Other analytics**: Add tracking scripts to `_includes/head.html`

## Performance Optimization

- Minified CSS
- Optimized images (use WebP format)
- Proper caching headers
- Fast loading times
- Core Web Vitals optimization

## Security

- HTTPS enforced on GitHub Pages
- No server-side processing
- Safe user-generated content handling
- CSP headers ready

## Mobile Responsive

The site is fully responsive and works on:
- Desktop (1200px+)
- Tablet (768px-1199px)
- Mobile (320px-767px)

## Contributing

Feel free to:
- Report issues
- Suggest improvements
- Submit pull requests
- Share feedback

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

If you need help:
1. Check the [Jekyll documentation](https://jekyllrb.com/docs/)
2. Review [GitHub Pages documentation](https://docs.github.com/en/pages)
3. Open an issue in this repository

---

**Built with ❤️ for the data engineering community**
