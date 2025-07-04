# Rella Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Rella landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">Rella</a>
```
- Replace "Rella" with your desired text
- Keep the classes to maintain the gradient effect

2. **Navigation Links:**
```html
<div class="hidden lg:flex space-x-8">
    <a href="#about" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">About</a>
    <!-- Additional links -->
</div>
```
- Update link text between `<a>` tags
- Maintain the `class` attributes for consistent styling

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">Rella - The Prettiest Truck Driver Around</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">{This Beauty is Breaking stereotypes one mile at a time.}</p>
```
- Update the h1 text while keeping the gradient classes
- Modify the paragraph text within the `<p>` tags
- The `md:` and `lg:` prefixes control responsive design at different screen sizes

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 rounded-2xl bg-white shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Hardworker</h3>
    <p class="text-gray-600">Dedicated to delivering excellence on every journey.</p>
</div>
```
- Update the h3 text for feature titles
- Modify paragraph text for feature descriptions
- Keep the surrounding classes for consistent styling

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#about">About</a>
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```
To update:
1. For internal sections, ensure the `href` matches the `id` of the target section
2. For external links, replace `#` with the full URL:
   ```html
   <a href="https://example.com">External Link</a>
   ```

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <!-- Facebook icon -->
    </a>
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <!-- Instagram icon -->
    </a>
</div>
```
Replace `#` with your social media profile URLs:
```html
<a href="https://facebook.com/your-profile">
```

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-6">Legal</h4>
    <ul class="space-y-4">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to policy pages:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Gradients**
   - Ensure all gradient classes remain intact:
   - `bg-gradient-to-r from-purple-600 to-pink-600`
   - `bg-clip-text text-transparent`

2. **Responsive Design Issues**
   - Check that responsive prefixes are preserved:
   - `text-4xl md:text-5xl lg:text-6xl`
   - `hidden lg:flex`

3. **Missing Styles**
   - Verify the Tailwind CDN link is present in the head:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

4. **Link Navigation Problems**
   - Ensure section IDs match their corresponding href attributes
   - Check for typos in URLs
   - Verify file paths for privacy and terms pages

Remember to test all changes across different screen sizes and browsers to ensure consistency.