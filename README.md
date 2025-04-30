# Brisbane Web Landing Page - Maintenance Guide

This guide will help you maintain and customize the Brisbane Web landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. Change the logo text:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">Brisbane Web</a>
```
Simply replace "Brisbane Web" with your desired text.

### Hero Section
Located at the top of the page with the main headline:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Best Websites In Brisbane
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Custom Websites For Your Business
</p>
```
- To modify text size, adjust the `text-4xl`, `text-5xl`, or `text-6xl` classes
- For different spacing, modify `mb-6` (margin-bottom) values
- Common spacing options: `mb-2`, `mb-4`, `mb-8`, `mb-12`

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-600">Intuitive interface designed for seamless navigation...</p>
</div>
```
To modify:
1. Change card background: Replace `bg-white` with colors like `bg-gray-50`
2. Adjust padding: Modify `p-8` (options: `p-4`, `p-6`, `p-12`)
3. Update shadow: Use `shadow-sm`, `shadow`, or `shadow-xl`

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Internal links (same page): Use `#section-id`
2. External links: Use full URL (e.g., `https://example.com`)
3. Local pages: Use relative paths (e.g., `/about.html`)

### Call-to-Action Buttons
Currently pointing to:
```html
<a href="https://sigmaseo.io" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Get Started Today
</a>
```
Replace `https://sigmaseo.io` with your desired URL.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` with proper paths:
```html
<li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in URLs
   - Ensure file names match exactly (case-sensitive)
   - Verify files are in the correct folder

2. **Styling Problems**
   - Make sure Tailwind CSS is properly loaded
   - Check for missing or mistyped class names
   - Verify closing tags match opening tags

3. **Mobile Menu Issues**
   - Ensure Alpine.js is properly loaded
   - Check `x-data` and `x-show` attributes
   - Verify mobile menu trigger button functionality

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct location
3. Ensure all required CDN links are working
4. Compare your changes against the original code

Remember to always backup your files before making changes!