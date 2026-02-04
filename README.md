# Ctrl Alpha - Quantitative Finance Club Website

Official website for Ctrl Alpha, the Quantitative Finance Club at IIIT Hyderabad.

Built with [Hugo](https://gohugo.io/) - a fast, modern static site generator.

## 🚀 Quick Start

### Local Development

1. Install Hugo (see [Hugo Installation Guide](https://gohugo.io/installation/))
2. Clone the repository
3. Run the development server:
   ```bash
   hugo server -D
   ```
4. Open `http://localhost:1313` in your browser

### Build for Production

```bash
hugo --minify
```

The built site will be in the `public/` directory.

## 📁 Project Structure

```
.
├── hugo.toml              # Site configuration
├── layouts/               # Page layouts
│   ├── _default/          # Default layouts (baseof, single, list)
│   ├── partials/          # Reusable components (header, footer)
│   ├── index.html         # Home page layout
│   ├── events/            # Event layouts
│   ├── members/           # Members layouts
│   └── moms/              # Minutes of Meetings layouts
├── static/css/            # Stylesheets
├── archetypes/            # Content templates
│   ├── moms.md            # MoM template
│   ├── events.md          # Event template
│   └── members.md         # Member template
├── content/               # All content
│   ├── events/            # Event pages
│   ├── members/           # Member information
│   └── moms/              # Minutes of Meetings
└── .github/workflows/     # GitHub Actions for deployment
```

## ✨ Adding Content

### Adding a New MoM (Minutes of Meeting)

The easiest way to add meeting minutes:

1. Copy the template file:
   ```bash
   cp archetypes/moms.md content/moms/YYYY-MM-DD-meeting-title.md
   ```
2. Edit the file:
   - Update the `title` field
   - Update the `date` field (format: YYYY-MM-DD)
   - Add attendees to the `attendees` list
   - Add action items to the `action_items` list
   - Write your meeting content in Markdown

**Example:**
```markdown
---
title: "Weekly Team Meeting"
date: 2024-03-15
draft: false
attendees:
  - Alice
  - Bob
  - Charlie
action_items:
  - Review trading strategy by Friday
  - Schedule workshop for next week
---

## Meeting Overview

Brief summary of the meeting...

## Discussion Points

### Budget Planning
We discussed the budget for upcoming events...
```

3. Commit and push - it will appear on the website automatically!

### Adding a New Event

1. Copy the template:
   ```bash
   cp archetypes/events.md content/events/YYYY-MM-DD-event-name.md
   ```
2. Fill in the event details
3. Commit and push

**Example:**
```markdown
---
title: "Introduction to Options Trading"
date: 2024-03-20
location: "Academic Building, Room 101"
draft: false
---

## About the Event

Join us for an exciting workshop on options trading...
```

### Adding a New Member

1. Copy the template:
   ```bash
   cp archetypes/members.md content/members/member-name.md
   ```
2. Fill in the member details
3. Commit and push

**Example:**
```markdown
---
name: "Jane Doe"
role: "Technical Lead"
year: "3rd Year, BTech CSE"
interests: "Quantitative Analysis, Python, ML"
draft: false
---
```

## 🎨 Design

The website features a clean, modern design that is:
- **Lightweight**: No heavy JavaScript frameworks
- **Fast**: Optimized for quick loading on any device
- **Accessible**: Works well on mobile, tablet, and desktop
- **Readable**: Clean typography with good contrast

Color scheme:
- **Black** (#1a1a1a): Headers and primary text
- **White** (#ffffff): Background
- **Orange** (#ff6b35): Accents and highlights
- **Gray** (#666): Secondary text

## 🔧 Customization

### Changing Site Title/Description
Edit `hugo.toml`:
```toml
title = "Your Club Name"

[params]
  description = "Your club description"
```

### Modifying Navigation
Edit the menu in `hugo.toml`:
```toml
[menu]
  [[menu.main]]
    name = "New Page"
    url = "/new-page/"
    weight = 5
```

### Updating Styles
Modify `static/css/style.css` to change colors, fonts, or layout.

## 📦 Deployment

This site is configured for automatic deployment to GitHub Pages:

1. Push to the `main` branch
2. GitHub Actions will automatically build and deploy
3. Your site will be live at `https://ctrl-alpha.github.io/`

### Manual Deployment
If you prefer manual deployment:
```bash
hugo --minify
# Upload contents of public/ to your hosting provider
```

## 🤝 Contributing

1. Create a new branch for your changes
2. Make your modifications
3. Test locally with `hugo server`
4. Submit a pull request

## 📝 Why Hugo?

- **No Ruby required**: Single binary, easy to install
- **Fast builds**: Sub-second build times
- **Markdown-based**: Easy content creation
- **Lightweight output**: Pure HTML/CSS, no heavy frameworks
- **GitHub Pages ready**: Works out of the box with GitHub Actions

## 📄 License

This website template is open source and available for use by other clubs.