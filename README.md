# Bow River Plumbing Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Bow River Plumbing landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Company Name -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">
    Bow River Plumbing  <!-- Update this text -->
</a>
```

**Styling Tips:**
- `text-2xl`: Controls font size
- `bg-gradient-to-r`: Creates right-flowing gradient
- `from-blue-500 to-teal-400`: Sets gradient colors

### Hero Section
The main landing section includes a title and subtitle:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-400 to-teal-300 bg-clip-text text-transparent">
    Trust Bow River Plumbing for Quality Solutions  <!-- Update main heading -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Expert Plumbing Solutions, Just a Click Away  <!-- Update subtitle -->
</p>
```

**Responsive Classes Explained:**
- `text-4xl md:text-5xl lg:text-6xl`: 
  - Default size: text-4xl
  - Medium screens: text-5xl
  - Large screens: text-6xl

### Features Section
To update service cards:

```html
<div class="bg-gray-800 rounded-xl p-8 shadow-lg hover:shadow-2xl transform hover:scale-105 transition-all duration-300">
    <h3 class="text-xl font-semibold mb-4">
        Complete Plumbing Solutions  <!-- Update service title -->
    </h3>
    <p class="text-gray-400">
        From repairs to installations...  <!-- Update service description -->
    </p>
</div>
```

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
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Example: `<a href="#new-section">New Section</a>`

### External Links
For email and website links:

```html
<a href="mailto:info@bowriverplumbing.com">Email Us</a>
<a href="https://www.bowriverplumbing.com">Visit Website</a>
```

To update:
1. Replace `info@bowriverplumbing.com` with your email
2. Replace `https://www.bowriverplumbing.com` with your website URL

## Linking Privacy and Terms Pages

### Footer Links
Current privacy and terms links:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html files
2. Update href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Section IDs should not contain spaces
   - Example: `<section id="contact">` matches `<a href="#contact">`

2. **Responsive Design Issues**
   - Check responsive classes are properly ordered (mobile first)
   - Correct order: `text-base md:text-lg lg:text-xl`
   - Incorrect order: `lg:text-xl md:text-lg text-base`

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     ```html
     bg-gradient-to-r
     from-[color] to-[color]
     bg-clip-text text-transparent
     ```

### Need Help?
- Double-check class names against [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all sections have unique IDs
- Test all links after updating
- View the page at different screen sizes to verify responsive design

Remember to always test changes in multiple browsers and screen sizes before deploying to production.