# Brisbane Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Brisbane Web Design landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Fixing Navigation Links](#fixing-navigation-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. Change company name:
```html
<!-- Find this section -->
<div class="text-2xl font-bold text-blue-600">
    Brisbane Web Design  <!-- Replace this text -->
</div>
```

2. Modify navigation items:
```html
<div class="hidden md:flex space-x-8">
    <!-- Each link can be updated here -->
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
</div>
```

### Hero Section
Update your main headline and subtitle:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight tracking-tight">
    Best Websites In Brisbane  <!-- Replace headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Professional web design solutions  <!-- Replace subtitle -->
</p>
```

### Features and Benefits Cards
Each card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-server text-4xl"></i>  <!-- Change icon here -->
    </div>
    <h3 class="text-xl font-bold mb-4">Free Hosting</h3>  <!-- Change title -->
    <p class="text-gray-600 leading-relaxed">
        Complimentary premium hosting  <!-- Change description -->
    </p>
</div>
```

### Understanding Tailwind Classes
Common classes used in this template:
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `text-{color}-{shade}`: Sets text color (blue-600, gray-900, etc.)
- `bg-{color}-{shade}`: Sets background color
- `p-{number}`: Sets padding (p-8 means padding of 2rem)
- `mb-{number}`: Sets margin bottom
- `rounded-{size}`: Controls border radius

## Fixing Navigation Links

### Internal Links
Current internal links use hashtags to scroll to sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Find the section ID you want to link to
2. Use `#section-id` in the href attribute
3. Ensure the target section has matching ID:
```html
<section id="features">  <!-- This ID matches the href="#features" -->
```

### External Links
Current external links to update:
```html
<!-- CTA Button -->
<a href="https://twd.com" class="inline-block bg-blue-600...">
    Get Started Today
</a>

<!-- Footer Email -->
<p class="text-gray-400">admin@twd.com</p>
```

Replace `https://twd.com` and `admin@twd.com` with your actual website and email.

## Adding Privacy and Terms Pages

### Step 1: Create New Files
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in href attributes
   - Ensure file names match exactly (case-sensitive)
   - Verify file locations are correct

2. **Styling Problems**
   - Make sure Tailwind CSS is properly loaded
   - Check for missing or mistyped class names
   - Maintain responsive classes (md:, lg:) for different screen sizes

3. **Icons Not Showing**
   - Verify Font Awesome is properly linked
   - Check icon class names against Font Awesome documentation
   - Ensure internet connection for CDN access

### Getting Help
If you need additional assistance:
1. Check the Tailwind CSS documentation for styling issues
2. Verify HTML syntax using an online validator
3. Test the page across different browsers
4. Ensure all files are saved and properly uploaded to your server

Remember to always make a backup before making significant changes to your website.