# Lake Coogee Web Design - Landing Page Maintenance Guide

This guide will help you maintain and customize the Lake Coogee Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Find this section:
```html
<div class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-600 bg-clip-text text-transparent">
    LCWD
</div>
```
Replace "LCWD" with your desired text.

2. **Navigation Menu**: Located in:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact Us</a>
</div>
```
Change menu item text while keeping the href attributes matching section IDs.

### Hero Section
Find the hero section starting with:
```html
<section class="pt-32 pb-24 relative overflow-hidden">
```
Update:
- Main heading: Replace "Lake Coogee Web Design"
- Subheading: Replace "Best Web Design In Perth"
- Button text: Modify "Get Started"

### Styling Tips
- Color gradients use `from-purple-600 to-blue-600`. To change colors:
  1. Find these classes in the code
  2. Replace with different Tailwind color classes (e.g., `from-blue-600 to-green-600`)
- Spacing uses patterns like `px-6 py-4`:
  - `px-6` means padding left/right
  - `py-4` means padding top/bottom
  - Numbers range from 1 to 16, representing 0.25rem to 4rem

## Managing Links

### Internal Links
Current internal links use section IDs:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact Us</a>
```

To update:
1. Find the target section ID: `<section id="features">`
2. Update the href to match: `<a href="#features">`

### External Links
The main external link is in the hero section:
```html
<a href="https/:lcwd.com" class="inline-block px-8 py-4...">
```

To update:
1. Replace `https/:lcwd.com` with your actual URL
2. Ensure the URL includes `https://`
3. Test the link after updating

### Email Link
Located in the contact section:
```html
<a href="mailto:graeme@graemephillips.info">Email Us Now</a>
```
Replace the email address while keeping the `mailto:` prefix.

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages:
1. Create new files:
   - Create `privacy.html`
   - Create `terms.html`

2. Update footer links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

3. Maintain consistent styling by copying these classes to new page links:
   - `hover:text-white`
   - `transition-colors`
   - `duration-300`

## Troubleshooting

### Common Issues:
1. **Broken Links**
   - Check for typos in href attributes
   - Verify file names match exactly
   - Ensure section IDs exist for internal links

2. **Styling Problems**
   - Verify Tailwind CDN link is working
   - Check for missing or mistyped classes
   - Maintain responsive classes (e.g., `md:` prefixes)

3. **Layout Issues**
   - Keep container classes: `container mx-auto px-6`
   - Maintain grid structure: `grid grid-cols-1 md:grid-cols-3`
   - Don't remove responsive classes

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify changes in multiple browsers
- Test on both desktop and mobile devices

Remember to always backup your files before making changes, and test thoroughly after each update.