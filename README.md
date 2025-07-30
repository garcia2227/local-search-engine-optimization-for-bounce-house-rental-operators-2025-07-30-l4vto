# JumperSEO Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the JumperSEO landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Logo Text**: Find this line in the header:
```html
<a href="/" class="text-2xl font-bold text-blue-600">JumperSEO</a>
```
Simply replace "JumperSEO" with your desired text.

2. **Navigation Items**: Located in the `<nav>` section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Other navigation items -->
</div>
```
To modify navigation text, update the text between `<a>` tags.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">Local Search Engine Optimization for Bounce House Rental Operators</h1>
<p class="text-2xl md:text-3xl text-gray-600 mb-12">We Turn Local Searches Into Booked Parties</p>
```
- To change heading size: Modify `text-4xl`, `text-5xl`, or `text-6xl`
- To adjust spacing: Modify `mb-6` (margin-bottom) values
- To change colors: Update `text-gray-600` with other Tailwind color classes

### Understanding Tailwind Classes
Common classes used in this template:
- `container`: Centers content and sets max-width
- `mx-auto`: Centers elements horizontally
- `px-6`: Adds horizontal padding
- `py-4`: Adds vertical padding
- `text-{size}`: Sets text size (xl, 2xl, etc.)
- `font-bold`: Sets font weight
- `bg-{color}`: Sets background color

## Managing Links

### Navigation Links
Current navigation links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Locate the link you want to change
2. Modify the `href` attribute:
   - For same-page sections: Use `#section-name`
   - For other pages: Use relative path (`/about.html`) or full URL (`https://example.com`)

### Call-to-Action Buttons
Main CTA buttons currently point to:
```html
<a href="https://jumperseo.net" class="inline-block px-8 py-4 bg-blue-600">
```

To update:
1. Replace `https://jumperseo.net` with your desired URL
2. Test the link after updating

## Adding Privacy and Terms Pages

### Step 1: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Add Proper Links
Replace the `#` placeholder:
```html
<li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 3: Create Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in URLs
   - Ensure files exist in the correct location
   - Verify that external URLs are accessible

2. **Styling Problems**
   - Check Tailwind CSS classes for typos
   - Ensure the Tailwind CDN link is working:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```
   - Verify class names match Tailwind's naming convention

3. **Responsive Issues**
   - Test on different screen sizes
   - Check responsive classes (md:, lg:, etc.)
   - Ensure the viewport meta tag is present:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

### Need Help?
- Double-check your changes against the original code
- Use browser developer tools (F12) to inspect elements
- Validate your HTML at [W3C Validator](https://validator.w3.org/)

Remember to always test your changes across different devices and browsers before publishing to production.