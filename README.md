# Ctrl Alpha - Quantitative Finance Club Website

Official website for Ctrl Alpha, the Quantitative Finance Club at IIIT Hyderabad.

## 🚀 Quick Start

### Local Development

1. Install Ruby and Bundler
2. Clone the repository
3. Install dependencies:
   ```bash
   bundle install
   ```
4. Run the development server:
   ```bash
   bundle exec jekyll serve
   ```
5. Open `http://localhost:4000` in your browser

## 📁 Project Structure

```
.
├── _config.yml           # Site configuration
├── _layouts/             # Page layouts
├── _includes/            # Reusable components (header, footer)
├── assets/css/           # Stylesheets
├── _events/              # Event pages
├── _members/             # Member information
├── _moms/                # Minutes of Meetings
├── index.html            # Home page
├── events.html           # Events listing page
├── members.html          # Members page
└── moms.html             # MoMs listing page
```

## ✨ Adding Content

### Adding a New Event

1. Create a new file in `_events/` directory
2. Name it: `YYYY-MM-DD-event-name.md`
3. Add front matter and content:

```markdown
---
title: Event Title
date: 2024-01-15
location: Room 101
excerpt: Brief description of the event.
---

Event content goes here in Markdown...
```

### Adding a New Member

1. Create a new file in `_members/` directory
2. Name it: `member-name.md`
3. Add front matter:

```markdown
---
name: Member Name
role: President
year: 4th Year, BTech CSE
interests: Trading, ML, Finance
---
```

### Adding Meeting Minutes (MoMs)

1. Create a new file in `_moms/` directory
2. Name it: `YYYY-MM-DD-meeting-title.md`
3. Use the template in `_moms/TEMPLATE.md` or add:

```markdown
---
title: Meeting Title
date: 2024-01-10
attendees:
  - Person 1
  - Person 2
action_items:
  - Action 1
  - Action 2
---

## Meeting content...
```

4. Commit and push - the MoM appears automatically!

## 🎨 Design

The website uses a minimal color scheme:
- **Black** (#1a1a1a): Primary text and headers
- **White** (#ffffff): Background
- **Orange** (#ff6b35): Accents and highlights

## 🔧 Customization

### Changing Site Title/Description
Edit `_config.yml`:
```yaml
title: Your Club Name
description: Your club description
```

### Modifying Navigation
Edit `_includes/header.html` to add/remove menu items.

### Updating Styles
Modify `assets/css/style.css` to change colors, fonts, or layout.

## 📦 Deployment

This site is configured for GitHub Pages:
1. Push to the main branch
2. Enable GitHub Pages in repository settings
3. Set source to "main branch"
4. Your site will be live at `https://username.github.io/repository-name/`

## 🤝 Contributing

1. Create a new branch for your changes
2. Make your modifications
3. Test locally with `bundle exec jekyll serve`
4. Submit a pull request

## 📄 License

This website template is open source and available for use by other clubs.