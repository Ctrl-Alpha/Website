# Ctrl Alpha Website - Complete Setup Guide

## Overview
This is a complete Jekyll-based static website for Ctrl Alpha, the Quantitative Finance Club at IIIT Hyderabad. The website features a minimal black, white, and orange color scheme and is designed to be easily extensible.

## Quick Start

### Prerequisites
- Ruby 3.2 or higher
- Bundler gem
- Git

### Installation
```bash
# Clone the repository
git clone https://github.com/Ctrl-Alpha/Website.git
cd Website

# Install dependencies
bundle install

# Run the development server
bundle exec jekyll serve

# Open http://localhost:4000 in your browser
```

## Website Structure

### Pages
1. **Home (`index.html`)**: Welcome page with club introduction and mission
2. **Events (`events.html`)**: Listing of all club events
3. **Members (`members.html`)**: Grid display of club members
4. **MoMs (`moms.html`)**: Minutes of Meetings listing

### Collections
The website uses Jekyll collections for modular content:
- `_events/`: Event pages
- `_members/`: Member information
- `_moms/`: Meeting minutes

### Layouts
- `default.html`: Base layout with header and footer
- `page.html`: Standard page layout
- `event.html`: Event-specific layout
- `mom.html`: Meeting minutes layout with action items

## Adding Content

### Adding a New Event

1. Create a new file in `_events/` directory
2. Name it: `YYYY-MM-DD-event-name.md`
3. Add front matter:

```yaml
---
title: Event Title
date: 2024-01-15
location: Room 101
excerpt: Brief description of the event.
---

Event content goes here in Markdown format...
```

### Adding a New Member

1. Create a new file in `_members/` directory
2. Name it: `member-name.md`
3. Add front matter:

```yaml
---
name: Member Name
role: President
year: 4th Year, BTech CSE
interests: Trading, ML, Finance
---
```

### Adding Meeting Minutes (MoMs)

This is the most important feature for minimal friction!

1. Create a new file in `_moms/` directory
2. Name it: `YYYY-MM-DD-meeting-title.md`
3. Copy the template from `_moms/TEMPLATE.md` or use this structure:

```yaml
---
title: Meeting Title
date: 2024-01-10
attendees:
  - Person 1
  - Person 2
action_items:
  - Action item 1
  - Action item 2
---

## Meeting Overview
Brief summary of the meeting...

## Key Discussions
### Topic 1
Discussion details...

## Decisions Made
1. Decision 1
2. Decision 2

## Next Steps
- Next step 1
- Next step 2
```

4. Commit and push - **the MoM will appear automatically!**

## Color Scheme

The website uses a minimal three-color palette:

- **Black** (#1a1a1a): Primary text, borders, and header
- **White** (#ffffff): Background and light text
- **Orange** (#ff6b35): Accents, highlights, and active states

## Customization

### Changing Site Information

Edit `_config.yml`:
```yaml
title: Your Club Name
description: Your club description
```

### Modifying Navigation

Edit `_includes/header.html` to add/remove menu items.

### Updating Styles

All styles are in `assets/css/style.css`. The CSS is organized by component for easy modification:
- Reset and Base Styles
- Header
- Navigation
- Main Content
- Cards
- Events/Members/MoMs specific styles
- Footer
- Responsive Design

### Adding New Pages

1. Create a new HTML or Markdown file in the root directory
2. Add front matter with layout:
```yaml
---
layout: page
title: Page Title
---
```
3. Add content
4. Update navigation in `_includes/header.html`

## Deployment

### GitHub Pages (Automatic)

The website includes a GitHub Actions workflow that automatically deploys to GitHub Pages when you push to the main branch.

**Setup Steps:**
1. Go to repository Settings → Pages
2. Under "Source", select "GitHub Actions"
3. Push to the main branch
4. Your site will be live at `https://ctrl-alpha.github.io/Website/`

### Manual Deployment

To build the site manually:
```bash
bundle exec jekyll build
```

The site will be generated in the `_site` directory.

## File Organization

```
.
├── .github/
│   └── workflows/
│       └── jekyll.yml          # GitHub Pages deployment
├── _config.yml                 # Jekyll configuration
├── _includes/
│   ├── header.html             # Site header and navigation
│   └── footer.html             # Site footer
├── _layouts/
│   ├── default.html            # Base layout
│   ├── page.html               # Page layout
│   ├── event.html              # Event layout
│   └── mom.html                # MoM layout
├── _events/                    # Event markdown files
├── _members/                   # Member markdown files
├── _moms/                      # Meeting minutes
│   └── TEMPLATE.md             # Template for new MoMs
├── assets/
│   └── css/
│       └── style.css           # Main stylesheet
├── index.html                  # Home page
├── events.html                 # Events listing
├── members.html                # Members page
├── moms.html                   # MoMs listing
├── Gemfile                     # Ruby dependencies
├── .gitignore                  # Git ignore rules
└── README.md                   # Project documentation
```

## Tips and Best Practices

### For MoMs (Minimal Friction)
- Always use the template from `_moms/TEMPLATE.md`
- Follow the naming convention: `YYYY-MM-DD-meeting-title.md`
- Keep the date format as `YYYY-MM-DD` in the front matter
- Action items will automatically appear in a highlighted section

### For Events
- Use descriptive titles
- Include location information
- Add an excerpt for the listing page

### For Members
- Use consistent formatting for roles
- Keep interests brief and relevant
- Update the member list regularly

## Troubleshooting

### Site not building?
- Check that all file names follow the correct format
- Verify front matter has valid YAML syntax
- Ensure dates are in `YYYY-MM-DD` format

### Changes not appearing?
- Clear your browser cache
- Check if Jekyll server is running
- Rebuild the site: `bundle exec jekyll build`

### Styling issues?
- Check `assets/css/style.css` for conflicting rules
- Verify CSS class names match HTML elements
- Use browser developer tools to inspect elements

## Contributing

When adding new features or content:
1. Create a new branch
2. Make your changes
3. Test locally with `bundle exec jekyll serve`
4. Submit a pull request

## Support

For issues or questions:
- Check this documentation first
- Review Jekyll documentation: https://jekyllrb.com/docs/
- Open an issue on GitHub

## License

This website template is open source and available for use by other clubs and organizations.

---

Built with ❤️ for Ctrl Alpha
