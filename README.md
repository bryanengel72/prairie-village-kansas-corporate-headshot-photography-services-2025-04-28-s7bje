# Landing Page Maintenance Guide

This guide will help you maintain and customize the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<a href="/" class="text-2xl font-bold">
    101Headshots  <!-- Update company name here -->
</a>
```

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Prairie Village, Kansas Corporate Headshot Photography Services  <!-- Update main heading -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Capturing confidence of Prairie Village's pros with premium photography.  <!-- Update subheading -->
</p>
```

#### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-800 rounded-2xl p-8">
    <h3 class="text-xl font-semibold mb-4">Pose Advice</h3>  <!-- Update feature title -->
    <p class="text-gray-400">Expert guidance to capture your most confident and professional angles.</p>  <!-- Update feature description -->
</div>
```

### Tailwind CSS Classes Explained

#### Common Class Patterns
- Spacing: `p-8` (padding), `m-8` (margin), `mb-4` (margin-bottom)
- Colors: `bg-gray-800` (background), `text-gray-400` (text color)
- Responsive Design: `md:text-5xl` (applies at medium screens and up)
- Hover Effects: `hover:shadow-xl hover:text-white`

To modify styles:
1. Find the element you want to change
2. Locate its class attribute
3. Add or modify classes following this pattern:
   ```html
   <!-- Original -->
   <div class="bg-gray-800 p-8">
   
   <!-- Modified for more padding -->
   <div class="bg-gray-800 p-12">
   ```

## Fixing Broken Links

### Current Link Inventory
```html
<!-- Navigation Menu Links -->
<a href="#features">Services</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Book Now</a>

<!-- Main CTA Link -->
<a href="https://www.101headshots.com">Schedule Your Session</a>

<!-- Email Link -->
<a href="mailto:bryan@101headshots.com">Contact Us</a>
```

### Updating Links
1. Internal Links (Same Page):
   ```html
   <!-- Format: -->
   <a href="#section-id">Link Text</a>
   
   <!-- Example: -->
   <a href="#features">Services</a>
   ```

2. External Links:
   ```html
   <!-- Format: -->
   <a href="https://full-website-url">Link Text</a>
   
   <!-- Example: -->
   <a href="https://www.101headshots.com">Schedule Your Session</a>
   ```

3. Email Links:
   ```html
   <!-- Format: -->
   <a href="mailto:email@domain.com">Contact Text</a>
   ```

## Linking Privacy and Terms Pages

### Current Footer Structure
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

### Adding Policy Links
1. Create your policy pages (privacy.html and terms.html)
2. Update the footer links:
   ```html
   <ul class="space-y-2">
       <li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
       <li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
   </ul>
   ```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in IDs
   ```html
   <!-- Section ID -->
   <section id="features">
   
   <!-- Matching Link -->
   <a href="#features">
   ```

2. **Responsive Design Issues**
   - Check media query classes (md:, lg:)
   - Test on different screen sizes
   ```html
   <!-- Example of responsive text -->
   <h1 class="text-4xl md:text-5xl lg:text-6xl">
   ```

3. **Style Inconsistencies**
   - Maintain consistent color schemes:
     - Primary gradient: `from-purple-500 to-pink-500`
     - Background: `bg-gray-900`
     - Text: `text-gray-100`, `text-gray-300`, `text-gray-400`

### Need Help?
- Double-check class names against [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all links work before deploying changes
- Test responsiveness using browser developer tools
- Maintain backup copies before making significant changes

Remember to test all changes thoroughly before pushing to production!