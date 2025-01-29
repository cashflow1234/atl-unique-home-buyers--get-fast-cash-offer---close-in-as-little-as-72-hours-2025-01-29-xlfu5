# ATL Unique Home Buyers Landing Page - Maintenance Guide

This guide will help you maintain and customize the ATL Unique Home Buyers landing page. Whether you're new to HTML and CSS or just getting started, follow these detailed instructions to make updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. Company Name:
```html
<!-- Find this div in the header -->
<div class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    ATL Unique Home Buyers  <!-- Change this text -->
</div>
```

2. Navigation Menu Items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change menu item text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

### Hero Section
To update the main headline and subtext:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Get Fast Cash Offer & Close in as Little as 72 Hours  <!-- Update headline here -->
</h1>
<p class="text-xl text-gray-700 mb-12 leading-relaxed">
    We buy homes in any condition...  <!-- Update description here -->
</p>
```

### Tailwind CSS Class Guide
Common classes explained:
- `text-xl`, `text-2xl`, etc.: Text size
- `mb-8`, `mt-12`, etc.: Margin spacing
- `py-24`, `px-4`, etc.: Padding
- `bg-white`: Background color
- `text-gray-700`: Text color
- `rounded-full`: Rounded corners
- `hover:shadow-lg`: Hover effects

To modify responsive design:
```html
<!-- Example of responsive classes -->
<div class="text-xl      <!-- Mobile size -->
    md:text-2xl         <!-- Medium screens -->
    lg:text-3xl">      <!-- Large screens -->
```

## Fixing Broken Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```

To update:
1. For internal sections, keep the `#` prefix
2. Ensure the ID matches in the section:
```html
<section id="features">  <!-- This ID must match the href -->
```

### Call-to-Action Links
Current form link:
```html
<a href="https://form.jotform.com/250276622130043">
```
To update:
1. Replace the JotForm URL with your new form URL
2. Verify the link works before publishing

### Email Links
Current email link:
```html
<a href="mailto:getoffer@atlfastcash.com">
```
To update:
1. Change email address after `mailto:`
2. Update displayed email text

## Linking Privacy and Terms Pages

### Footer Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-sm">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. Broken Layouts
- Check for missing closing tags
- Verify all divs are properly nested
- Ensure responsive classes are correctly ordered (mobile first)

2. Links Not Working
- Verify href attributes start with `#` for internal links
- Check for typos in URLs
- Ensure section IDs match exactly with href values

3. Styles Not Applying
- Check for typos in Tailwind class names
- Verify the Tailwind CSS CDN link is working
- Make sure classes are space-separated

### Need Help?
If you encounter issues:
1. Use browser inspect tools (F12) to check for errors
2. Verify all changes against the original code
3. Test on multiple devices and browsers
4. Keep a backup of the original files before making changes

Remember to always test your changes in a development environment before pushing to production.