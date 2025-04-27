# Landing Page Maintenance Guide

This guide will help you maintain and customize the Hoogwerker Huren landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold text-blue-600">Hoogwerker<span class="text-gray-900">Huren</span></a>
```
To modify the header:
1. Change the company name by editing the text between `<a>` tags
2. Adjust text size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)
3. Change colors by modifying `text-blue-600` (options: text-blue-[50-900])

### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Hoogwerker Huren Groningen
    <span class="block text-blue-600 mt-2">Tijdelijk 10% Korting!</span>
</h1>
```
To update the hero section:
1. Edit the main heading text
2. Modify the promotional text within the `<span>` tag
3. Adjust responsive text sizes:
   - Mobile: `text-4xl`
   - Tablet: `md:text-5xl`
   - Desktop: `lg:text-6xl`

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Snelle Levering</h3>
    <p class="text-gray-600">Binnen 24 uur geleverd in heel Groningen.</p>
</div>
```
To modify features:
1. Locate the feature card you want to change
2. Update the heading in the `<h3>` tag
3. Modify the description in the `<p>` tag
4. Adjust spacing using `mb-4` (margin-bottom) or `p-8` (padding) classes

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Voordelen</a>
    <a href="#pricing" class="text-gray-600 hover:text-blue-600">Prijzen</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600">Contact</a>
</div>
```
To update navigation links:
1. Identify the section ID you want to link to
2. Update the `href` attribute with the corresponding ID
3. Example: `<a href="#new-section">New Section</a>`

### External Links
Current external link:
```html
<a href="https://hansschuiling.nl" class="bg-blue-600 text-white px-6 py-2">Direct Huren</a>
```
To update external links:
1. Replace `https://hansschuiling.nl` with your desired URL
2. Ensure the URL includes `https://` or `http://`
3. Test the link after updating

## Linking Privacy and Terms Pages

### Footer Links Section
Current footer structure:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Links</h3>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
    </ul>
</div>
```
To add privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - IDs should not contain spaces
   - Example: `href="#contact"` links to `id="contact"`

2. **Responsive Design Issues**
   - Check responsive classes are properly ordered:
     ```html
     class="text-base md:text-lg lg:text-xl"
     ```
   - Use browser dev tools to test different screen sizes

3. **Style Changes Not Applying**
   - Verify Tailwind CSS is properly loaded
   - Check class spelling matches Tailwind conventions
   - Use more specific classes to override existing styles

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all files are in the correct directory
3. Ensure all links begin with either `#`, `/`, or `https://`
4. Test the page in multiple browsers

Remember to always backup your files before making changes, and test all modifications in a development environment first.