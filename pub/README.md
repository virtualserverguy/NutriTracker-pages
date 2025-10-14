# FuelFlow Website

Jekyll website for FuelFlow - Real-time nutrition tracking for ultramarathon runners.

## Setup

### Prerequisites

- Ruby (2.7 or higher)
- Bundler

### Installation

1. Clone this repository
1. Install dependencies:
   
   ```bash
   bundle install
   ```
1. Run the development server:
   
   ```bash
   bundle exec jekyll serve
   ```
1. Open your browser to `http://localhost:4000`

## Project Structure

```
.
├── _config.yml           # Site configuration
├── index.md             # Homepage
├── about.md             # About page
├── features.md          # Features page
├── screenshots.md       # Screenshots gallery
├── faq.md              # Frequently asked questions
├── privacy.md          # Privacy policy
├── contact.md           # Contact page
├── assets/
│   └── images/
│       └── screenshots/ # Screenshot images
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

## Adding Screenshots

1. Create the directory structure:
   
   ```bash
   mkdir -p assets/images/screenshots
   ```
1. Add your screenshot images to `assets/images/screenshots/`:
- `iphone-food-library.png`
- `iphone-active-run.png`
- `iphone-hourly-breakdown.png`
- `iphone-log-food.png`
- `iphone-goals.png`
- `iphone-export.png`
- `iphone-export-detail.png`
- `watch-active-run.png`
- `watch-food-list.png`
- `watch-water.png`
- `watch-stats.png`
1. Screenshots should be:
- iPhone: 1170 x 2532 pixels (or actual device resolution)
- Apple Watch: 396 x 484 pixels for 44mm (or actual device resolution)

## Customization

### Update Race Results

Edit `about.md` and replace the example races with your actual UltraSignup results.

### Update Email Addresses

The following email addresses are used throughout the site:

- `info@fuelflow.run` - General inquiries
- `support@fuelflow.run` - Technical support

### Update Social Links

Edit `_config.yml` to add your social media usernames.

### Add App Store Link

Once your app is published, search for `Download on App Store` and replace `#` with your actual App Store URL.

## Deployment

### GitHub Pages

1. Push to GitHub
1. Enable GitHub Pages in repository settings
1. Set source to main branch
1. Your site will be available at `https://yourusername.github.io/repository-name`

### Custom Domain (fuelflow.run)

1. Add a CNAME file with `fuelflow.run` content
1. Configure DNS:
- Add A records pointing to GitHub Pages IPs
- Or add CNAME record pointing to `yourusername.github.io`
1. Enable HTTPS in GitHub Pages settings

## License

Copyright © 2025 FuelFlow. All rights reserved.