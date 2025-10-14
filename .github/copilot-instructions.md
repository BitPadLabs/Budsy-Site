# GitHub Copilot Instructions for Budsy-Site

## Project Overview
This is the official website repository for **BudsyApp** - a medical marijuana tracking application. The site is built with Jekyll and deployed via GitHub Pages.

**Site URL**: https://www.budsyapp.com  
**Repository**: BitPadLabs/Budsy-Site  
**Organization**: BitPadLabs LLC

## Technology Stack
- **Static Site Generator**: Jekyll 3.x (GitHub Pages compatible)
- **Theme**: Minima 2.5
- **Markup**: Markdown + Liquid templating
- **Styling**: SCSS/Sass
- **Hosting**: GitHub Pages
- **Ruby Version**: 2.6.0+ (compatible with Ruby 3.4+)
- **Deployment**: Automated via GitHub Actions

## Site Structure

### Core Files
- `_config.yml` - Site configuration, must be changed to see updates (requires server restart)
- `index.md` - Homepage content
- `Gemfile` - Ruby dependencies (use `github-pages` gem for compatibility)
- `CNAME` - Custom domain configuration

### Key Directories
- `_layouts/` - HTML templates for page structures
  - `default.html` - Base layout for all pages
  - `post.html` - Layout for blog posts
- `_includes/` - Reusable HTML partials
  - `header.html` - Site navigation and header
  - `footer.html` - Site footer with contact/social links
  - `head.html` - Meta tags, stylesheets, SEO
  - `social.html` - Social media links component
- `_posts/` - Blog posts (Markdown files)
- `_site/` - Generated static site (DO NOT EDIT - auto-generated)
- `assets/` - Static assets (CSS, images, JavaScript)
  - `assets/css/style.scss` - Main stylesheet
  - `assets/img/` - Images and graphics

### Important Pages
- `ios-download.html` - App Store download/redirect page
- `blog.html` - Blog listing page
- `privacy.md` - Privacy policy
- `terms.md` - Terms of service
- `update.json` - App update configuration

## Blog System

The blog system uses Jekyll's built-in posts feature with custom layouts and styling. Posts are displayed on the `/blog` page and support two distinct formats: standard posts and gallery posts.

### Blog Page
- Located at `blog.html` in the root directory
- Lists all posts in reverse chronological order
- Shows featured image, title, excerpt, date, and categories
- Responsive grid layout with post cards

### Post Layout (`_layouts/post.html`)
The post layout includes:
- Featured image display
- Title with custom Budsy styling
- Post metadata (date, author)
- Main content area
- Optional gallery slider (for event posts)
- Automatic slideshow with navigation controls
- Responsive design for all screen sizes

## Blog Post Conventions

### File Naming
Posts MUST follow this format: `YYYY-MM-DD-title-slug.md`
Example: `2025-09-19-1.12-release-notes.md`

### Post Type 1: Standard Post (No Gallery)

Use for: Release notes, announcements, updates, general blog content

```yaml
---
layout: post
title: "Your Post Title"
author: Budsyapp Team
categories: [category1, category2]
tags: [tag1, tag2, tag3]
date: YYYY-MM-DD
excerpt: "Brief description for SEO and previews (will appear on blog listing page)"
image: /assets/img/image-name.png
---

Your markdown content goes here...
```

**Example**: `2025-09-19-1.12-release-notes.md`
```yaml
---
layout: post
title: "What's New in BudsyApp v1.12"
author: Budsyapp Team
categories: [product, update]
tags: [budsyapp, cannabis, release-notes]
date: 2025-09-19
excerpt: "BudsyApp v1.12 is a major update with purchase log improvements, ECS education, and more."
image: /assets/img/budsy-app-icon.png
---
```

### Post Type 2: Gallery Post (With Event Photos)

Use for: Events, community outreach, photo recaps

```yaml
---
layout: post
title: "Event Name"
author: Budsyapp Team
categories: [events, community, outreach]
tags: [budsyapp, cannabis, event, community]
date: YYYY-MM-DD
excerpt: "Brief description of the event"
image: /assets/img/events/event-main-image.jpg
gallery:
  - /assets/img/events/event-photo-1.jpg
  - /assets/img/events/event-photo-2.jpg
  - /assets/img/events/event-photo-3.jpg
  - /assets/img/events/event-photo-4.jpg
---

Your event description and recap goes here...
```

**Example**: `2025-09-28-tea-and-terpenes.md`
```yaml
---
layout: post
title: "Join BudsyApp at Tea & Terpenes Event"
author: Budsyapp Team  
categories: [events, community, outreach]
tags: [budsyapp, cannabis, education, event, terpenes, community]
date: 2025-09-28
excerpt: "Come meet the BudsyApp team at Tea & Terpenes!"
image: /assets/img/events/2025-09-28-tea-and-terpenes.jpeg
gallery:
  - /assets/img/events/2025-09-28-tea-and-terpenes.jpeg
  - /assets/img/events/2025-09-28-tea-and-terpenes-2.JPG
  - /assets/img/events/2025-09-28-tea-and-terpenes-3.jpeg
  - /assets/img/events/2025-09-28-tea-and-terpenes-4.png
---
```

### Gallery Features
When `gallery` is included in front matter:
- Automatic slideshow appears at the end of the post
- Navigation controls (prev/next arrows)
- Dot indicators for each image
- Auto-advance every 5 seconds
- Click dots to jump to specific images
- Responsive and mobile-friendly
- Displays "Event Gallery" heading

### Standard Categories
- `product` - Product announcements
- `release` - Release notes
- `update` - App updates
- `events` - Community events
- `event` - Single event (alternative)
- `outreach` - Community outreach
- `education` - Educational content
- `community` - Community-focused content

### Standard Tags
- `budsyapp` - Always include for app-related content
- `cannabis` - Cannabis-related topics
- `release-notes` - For version releases
- `community` - Community engagement
- `education` - Educational material
- `event` - Event-related content
- `terpenes` - Terpene education
- `dispensary` - Dispensary-related content

## Development Workflow

### Local Development
```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve --livereload

# Serve on specific host/port
bundle exec jekyll serve --host 127.0.0.1 --port 4000 --livereload

# Kill existing Jekyll processes if port is in use
pkill -f jekyll

# Clean build (if needed)
bundle exec jekyll clean
bundle exec jekyll build
```

### Important Notes
- Changes to `_config.yml` require server restart
- Browser cache issues: Use hard refresh (Cmd+Shift+R on Mac)
- Live reload helps auto-refresh during development
- Generated files in `_site/` are ignored by git

## GitHub Pages Deployment

### Automated Workflow
- Deployment managed via `.github/workflows/jekyll.yml`
- Triggers on push to `main` branch
- Can also be triggered manually via Actions tab
- Uses GitHub Pages environment for deployment

### Build Process
1. Checkout repository
2. Setup Ruby environment
3. Install dependencies via Bundler
4. Build Jekyll site
5. Deploy to GitHub Pages

## Content Guidelines

### Writing Blog Posts

#### Standard Posts (No Gallery)
1. Create file: `_posts/YYYY-MM-DD-post-title.md`
2. Add front matter with layout, title, author, categories, tags, date, excerpt, image
3. Write content in Markdown
4. Add featured image to `assets/img/`
5. Commit and push to trigger deployment

#### Gallery Posts (Event Photos)
1. Create file: `_posts/YYYY-MM-DD-event-name.md`
2. Add front matter including `gallery` array with image paths
3. Upload all event photos to `assets/img/events/`
4. List images in `gallery` array in desired order
5. First image in gallery typically matches the `image` field
6. Write event description/recap in Markdown
7. Gallery slider will automatically appear at end of post
8. Commit and push to trigger deployment

### Adding Images

#### For Standard Posts
- Store in `assets/img/`
- Use descriptive filenames (e.g., `budsy-app-icon.png`, `feature-screenshot.png`)
- Reference with absolute path: `/assets/img/filename.png`

#### For Event/Gallery Posts
- Store in `assets/img/events/`
- Use date-prefixed filenames (e.g., `2025-09-28-tea-and-terpenes.jpeg`)
- Include multiple photos from different angles
- Reference in gallery array with absolute paths
- Keep file sizes reasonable for web performance (optimize before upload)
- Supported formats: JPG, JPEG, PNG

#### Image Best Practices
- **Filenames**: Use lowercase, hyphens for spaces, include date for events
- **Sizing**: Optimize images (recommended max width: 1920px)
- **Alt text**: Automatically generated from post title for featured images
- **Gallery order**: First image should be the best/main photo
- **Consistency**: Use similar aspect ratios within a gallery when possible

### Styling Guidelines
- Primary color: `#89b153` (Budsy green)
- Use semantic HTML5 elements
- Maintain responsive design principles
- Follow existing component patterns in `_includes/`

## Configuration Management

### Site Variables (in `_config.yml`)
- `title`: Site title
- `description`: Site description for SEO
- `url`: Production URL (https://www.budsyapp.com)
- `baseurl`: Leave empty (no subdirectory)
- `app.store_url`: Apple App Store link
- `app.id`: iOS App ID (6748842648)
- `contact_email`: info@budsyapp.com

### Contributors
- hrcassels (Lead Developer)
- Severswoed (Co-Developer)

## SEO & Social Media

### Plugins Used
- `jekyll-feed` - RSS feed generation
- `jekyll-sitemap` - XML sitemap
- `jekyll-seo-tag` - Meta tags and structured data

### Social Accounts
- Twitter: @budsyapp
- GitHub Org: BitPadLabs
- Facebook: /people/Budsyapp/61579918078091/

## Issue Templates

The repository includes structured issue templates in `.github/ISSUE_TEMPLATE/`:

1. **bug_report.yml** - Bug reports for app or website
2. **feature_request.yml** - Feature enhancement requests
3. **educational_content.yml** - Educational content proposals
4. **vendor_data.yml** - Vendor/dispensary data submissions

When creating issues, use these templates for consistency.

## Common Tasks

### Adding a New Blog Post

#### Creating a Standard Blog Post
1. Create file: `_posts/YYYY-MM-DD-post-title.md`
2. Add front matter:
```yaml
---
layout: post
title: "Your Post Title"
author: Budsyapp Team
categories: [product, update]
tags: [budsyapp, cannabis]
date: YYYY-MM-DD
excerpt: "Brief description for previews"
image: /assets/img/your-image.png
---
```
3. Write Markdown content below front matter
4. Add featured image to `assets/img/`
5. Test locally with `bundle exec jekyll serve`
6. Commit and push to deploy

#### Creating a Gallery/Event Post
1. Create file: `_posts/YYYY-MM-DD-event-name.md`
2. Add front matter with gallery array:
```yaml
---
layout: post
title: "Event Name"
author: Budsyapp Team
categories: [events, community, outreach]
tags: [budsyapp, event, community]
date: YYYY-MM-DD
excerpt: "Event description"
image: /assets/img/events/event-main.jpg
gallery:
  - /assets/img/events/event-photo-1.jpg
  - /assets/img/events/event-photo-2.jpg
  - /assets/img/events/event-photo-3.jpg
---
```
3. Upload all event photos to `assets/img/events/`
4. Write event recap/description in Markdown
5. Gallery slideshow will automatically appear at the end
6. Test locally to verify all images load
7. Commit and push to deploy

### Updating Site Configuration
1. Edit `_config.yml`
2. Restart Jekyll server locally to test
3. Commit and push changes
4. GitHub Actions will rebuild and deploy

### Modifying Layouts or Includes
1. Edit files in `_layouts/` or `_includes/`
2. Test locally with `bundle exec jekyll serve`
3. Verify responsive design
4. Commit and push

### Adding CSS Styles
1. Edit `assets/css/style.scss`
2. Use existing color scheme and patterns
3. Test across different screen sizes
4. Minified automatically via Sass configuration

## Troubleshooting

### Common Issues
- **Port already in use**: Run `pkill -f jekyll` to kill existing processes
- **Config changes not showing**: Restart Jekyll server
- **Styles not updating**: Clear browser cache (Cmd+Shift+R)
- **Build fails**: Check for YAML syntax errors in front matter or `_config.yml`
- **Images not showing**: Verify absolute path starts with `/assets/`

### GitHub Pages Specific
- Check Actions tab for deployment status
- Ensure `github-pages` gem is used (not individual Jekyll)
- Verify `_config.yml` has correct `url` setting
- Custom domain requires valid `CNAME` file

## Best Practices

### Code Organization
- Keep layouts semantic and minimal
- Reuse components via includes
- Use Liquid conditionals sparingly
- Comment complex template logic

### Content Management
- Use meaningful categories and tags
- Write descriptive commit messages
- Keep image file sizes optimized
- Maintain consistent post formatting

### Version Control
- Never commit `_site/` directory
- Keep `vendor/bundle/` in gitignore
- Review changes before pushing to `main`
- Use descriptive branch names for features

### Performance
- Optimize images before upload
- Use compressed Sass output
- Minimize plugin usage
- Leverage browser caching

## Security & Privacy

- No sensitive data in repository
- Environment variables for secrets (if needed)
- Privacy policy and terms of service maintained
- Compliant with GitHub Pages ToS
- HTTPS enforced via GitHub Pages

## Contact & Support

- **Email**: info@budsyapp.com / budsyapp@gmail.com
- **GitHub Issues**: Use templates for structured feedback
- **Contributors**: @hrcassels, @Severswoed

---

*Last Updated: October 2025*
