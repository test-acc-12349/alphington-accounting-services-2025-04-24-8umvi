# Alphington Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Alphington Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold text-gray-800">Alphington</a>
```
To update the company name, modify the text between the `<a>` tags.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    We transform numbers into opportunities
</h1>
<p class="text-xl text-gray-600 mb-10 leading-relaxed">
    Professional accounting services tailored to help your business thrive and grow
</p>
```
- Update the main heading by changing the text within the `<h1>` tags
- Modify the subheading by updating the text within the `<p>` tags

### Tailwind CSS Class Modifications

#### Understanding Responsive Classes
In this landing page, responsive classes follow this pattern:
- Default (mobile): `text-4xl`
- Medium screens (md): `md:text-5xl`
- Large screens (lg): `lg:text-6xl`

Example:
```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">

<!-- To make text smaller -->
<h1 class="text-3xl md:text-4xl lg:text-5xl">
```

#### Common Tailwind Classes Used
- Text colors: `text-gray-900`, `text-blue-600`
- Background colors: `bg-white`, `bg-blue-600`
- Padding: `p-8`, `py-24`, `px-6`
- Margins: `mb-6`, `mt-12`
- Flex properties: `flex`, `items-center`
- Grid properties: `grid`, `grid-cols-1`, `md:grid-cols-3`

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the link you want to change
2. Modify the `href` attribute
3. For external links, use complete URLs: `href="https://example.com"`
4. For internal links, use `#section-id`: `href="#services"`

### Call-to-Action Links
```html
<!-- Update this URL -->
<a href="https://theaccountants.com" class="inline-flex items-center...">
```
Replace `https://theaccountants.com` with your desired URL.

## Linking Privacy and Terms Pages

### Current Footer Structure
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Adding Privacy and Terms Links
1. Create your privacy.html and terms.html files
2. Update the footer links:
```html
<ul class="space-y-2">
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure the Tailwind CDN link is working:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

2. **Non-Working Links**
   - Verify file paths are correct
   - Ensure section IDs match link href attributes
   - Check for proper URL formatting in external links

3. **Responsive Issues**
   - Test on different screen sizes
   - Verify responsive classes (md:, lg:) are properly set
   - Check the viewport meta tag is present:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

### Need Help?
- Double-check all modifications against the original code
- Use browser developer tools (F12) to inspect elements
- Ensure all files are in the correct directory structure
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to always backup your files before making changes, and test all modifications across different browsers and devices.