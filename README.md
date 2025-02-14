# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<div class="text-2xl font-bold text-blue-600">
    Texas Web Design  <!-- Change this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Update your main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Best Websites In Texas  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Creating stunning, high-performance websites that drive results  <!-- Subheading -->
</p>
```

### Tailwind CSS Tips
- Font sizes use classes like `text-xl`, `text-2xl`, etc.
- Colors use format `text-{color}-{shade}` (e.g., `text-blue-600`)
- Spacing uses `m-` for margin and `p-` for padding
- Responsive classes start with screen sizes: `md:` or `lg:`

Example of changing colors:
```html
<!-- Original blue button -->
<a href="https://twd.com" class="inline-block bg-blue-600 text-white">

<!-- Changed to green -->
<a href="https://twd.com" class="inline-block bg-green-600 text-white">
```

## Managing Links

### Navigation Menu Links
Current internal links point to page sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. For internal sections, keep the `#` prefix
2. For external pages, use full URLs
3. For local pages, use relative paths

Example:
```html
<!-- Internal section -->
<a href="#about">About Us</a>

<!-- External link -->
<a href="https://example.com">Visit Us</a>

<!-- Local page -->
<a href="./about.html">About Page</a>
```

### Call-to-Action Buttons
Update the main CTA buttons:
```html
<!-- Hero section button -->
<a href="https://twd.com" class="inline-block bg-blue-600...">
    Get Started Today
</a>

<!-- Change to your actual URL -->
<a href="https://your-domain.com/contact" class="inline-block bg-blue-600...">
    Get Started Today
</a>
```

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the links:
```html
<li><a href="./privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="./terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Creating Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling

Example structure for policy pages:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body>
    <!-- Copy header section -->
    
    <main class="pt-32 px-6 container mx-auto">
        <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure container divs are properly nested

2. **Links Not Working**
   - Verify file paths are correct
   - Check for typos in URLs
   - Ensure section IDs match their href attributes

3. **Responsive Issues**
   - Test with different screen sizes
   - Verify responsive classes (md:, lg:) are correct
   - Check for conflicting classes

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Font Awesome Icons](https://fontawesome.com/icons)

Remember to always test your changes across different devices and browsers before publishing updates to your live site.