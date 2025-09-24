# n8n Agency Landing Page - Maintenance Guide

This guide will help you maintain and customize the n8n Agency landing page. It's designed for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Find this line in the header:
```html
<a href="/" class="text-2xl font-bold text-blue-600">n8n Agency</a>
```
Replace "n8n Agency" with your desired text.

2. **Navigation Menu Items**: Located in:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Other menu items -->
</div>
```
Modify the text between `<a>` tags to change menu items.

### Hero Section
Find the main headline and subtitle:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">n8n automation for any business</h1>
<p class="text-xl text-gray-600 mb-8">Streamline your workflows...</p>
```
- Change the h1 text to update your main headline
- Modify the paragraph text for your subtitle

### Tailwind CSS Classes Explained
Common classes used in this template:
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `font-[weight]`: Controls text weight (bold, semibold, etc.)
- `bg-[color]`: Sets background color
- `text-[color]`: Sets text color
- `p-[size]`: Sets padding
- `m-[size]`: Sets margin
- `rounded-[size]`: Controls border radius

Example modification:
```html
<!-- Original -->
<div class="bg-white rounded-xl p-8">

<!-- Modified for larger padding and different background -->
<div class="bg-gray-50 rounded-xl p-12">
```

## Managing Links

### Navigation Links
All navigation links are found in two places:

1. **Header Navigation**:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

2. **Call-to-Action Buttons**:
```html
<a href="https://test.com" class="inline-block px-8 py-4 bg-blue-600">
```
Replace `https://test.com` with your actual URL.

### Email Links
Find and update all email links:
```html
<a href="mailto:test@test.com">test@test.com</a>
```
Replace `test@test.com` with your actual email address.

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
- Check that all href attributes start with either:
  - `#` for page sections (e.g., `#features`)
  - `https://` for external links
  - Relative paths for local pages (e.g., `privacy.html`)

2. **Styling Issues**
- If styles aren't applying:
  - Verify the Tailwind CDN link is present in the head section
  - Check for typos in class names
  - Ensure classes are space-separated

3. **Responsive Design**
- If mobile layout breaks:
  - Check for `md:` prefixed classes
  - Ensure the viewport meta tag is present:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Need Help?
- Double-check all changes against the original code
- Use browser developer tools (F12) to inspect elements
- Test on multiple devices and browsers
- Keep a backup of the original code before making changes

Remember to always test your changes in a development environment before pushing to production.