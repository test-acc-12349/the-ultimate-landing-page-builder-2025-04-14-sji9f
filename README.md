# Landing Page Maintenance Guide

This guide will help you maintain and customize the LPBuilder landing page. Follow these detailed instructions to make common updates while preserving the page's responsive design and functionality.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**: Find this line and change "LPBuilder" to your brand name:
```html
<div class="text-2xl font-bold text-blue-600">LPBuilder</div>
```

2. **Navigation Links**: Located in the header's `<nav>` element:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
To modify link text, simply change the text between `<a>` tags.

### Hero Section
Find the main headline and subheading in the first `<section>` after `<main>`:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    The Ultimate Landing Page Builder
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Create stunning landing pages in minutes
</p>
```

**Tailwind CSS Tips:**
- `text-4xl` to `text-6xl`: Controls text size at different breakpoints
- `md:` prefix: Applies styles on medium screens and larger
- `mb-6`: Adds margin bottom (spacing)

### Features and Benefits Sections
Each feature/benefit card follows this structure:
```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <!-- Icon container -->
    <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-600">Feature description text here.</p>
</div>
```

To update:
1. Change the title text in the `<h3>` tag
2. Modify the description in the `<p>` tag
3. Keep the existing classes to maintain styling

## Managing Links

### Identifying Link Types
The page contains several types of links:

1. **Navigation Links** (internal):
```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">
```
- Update `href="#section-name"` to match your section IDs

2. **Call-to-Action Links** (external):
```html
<a href="https://example.com" class="inline-block px-8 py-4 bg-blue-600 text-white">
```
- Replace `https://example.com` with your actual URL

3. **Footer Links**:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">
```
- Replace `#` with actual URLs

### Updating Links Step-by-Step
1. Identify the link you want to update
2. Locate it in the HTML code
3. Change the `href` attribute value:
   - For internal links: `href="#section-id"`
   - For external links: `href="https://your-url.com"`
4. Test the link to ensure it works

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the Legal section in the footer:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
- Ensure section IDs match the href values
- Section IDs should not include spaces
- Example: `href="#contact"` matches `id="contact"`

2. **Styling Issues**
- Don't remove Tailwind classes unless you're sure about their purpose
- Keep responsive classes (starting with `md:` or `lg:`)
- Maintain the existing class order for consistent styling

3. **Layout Problems**
- Check that you haven't removed important container divs
- Maintain the grid structure in features/benefits sections
- Keep the `container mx-auto px-6` classes on main sections

Remember to test all changes across different screen sizes using your browser's developer tools.

Need help? Contact our support team at support@example.com.