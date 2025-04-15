# Landing Page Maintenance Guide

This guide will help you maintain and customize the ComputerBril.org landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## 1. Updating Text and Tailwind CSS Classes

### Main Content Sections

#### Header/Navigation
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold text-blue-600">ComputerBril.org</a>
```
To update:
- Change the website name by modifying the text between `<a>` tags
- Adjust text size using `text-2xl` (options: text-sm, text-lg, text-3xl)
- Modify brand color by changing `text-blue-600` (options: text-red-600, text-green-600)

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Wat is beter: Een Computerbril of Multifocale bril?
</h1>
```
To update:
- Change headline text between the `<h1>` tags
- Responsive text sizes are controlled by:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Tailwind CSS Tips for Beginners

1. Spacing Classes:
   - `px-4`: Horizontal padding
   - `py-4`: Vertical padding
   - `mb-8`: Margin bottom
   - Numbers range from 1-16 (smallest to largest)

2. Color Classes:
   - Format: `{type}-{color}-{shade}`
   - Example: `bg-blue-600`, `text-gray-900`
   - Common types: bg (background), text (text color)

3. Responsive Design:
   - Prefix classes with:
     - `sm:` (640px and up)
     - `md:` (768px and up)
     - `lg:` (1024px and up)

## 2. Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#voordelen">Voordelen</a>
    <a href="#vergelijking">Vergelijking</a>
    <a href="#faq">FAQ</a>
    <a href="https://computerbril.org/winkel">Shop Nu</a>
</div>
```

To update:
1. Internal links (starting with #):
   - Match the `href` with section IDs in the page
   - Example: `href="#voordelen"` links to `<section id="voordelen">`

2. External links:
   - Replace `https://computerbril.org/winkel` with your shop URL
   - Always include `https://` for external links

### Common Link Issues
- Verify all `href` attributes have valid destinations
- Test internal links scroll to correct sections
- Confirm external links open in correct window/tab

## 3. Linking Privacy and Terms Pages

### Footer Links Section
Current structure:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Terms & Conditions</a></li>
</ul>
```

To add privacy and terms pages:

1. Create new pages:
   ```html
   privacy.html
   terms.html
   ```

2. Update footer links:
   ```html
   <li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
   <li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Terms & Conditions</a></li>
   ```

3. Maintain consistent styling:
   - Keep the `hover:text-blue-400` class
   - Preserve the `transition-colors duration-300` animation

## Troubleshooting Tips

1. Broken Styles
   - Verify Tailwind CSS link is working:
   ```html
   <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
   ```
   - Check for typos in class names
   - Use browser inspector to debug styles

2. Non-working Links
   - Confirm file paths are correct
   - Check for missing or extra slashes
   - Verify file extensions (.html) are included

3. Responsive Issues
   - Test on multiple screen sizes
   - Verify responsive classes (sm:, md:, lg:) are correct
   - Use browser dev tools to test different viewports

## Additional Resources

- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML Links Guide](https://www.w3schools.com/html/html_links.asp)
- [Responsive Design Basics](https://web.dev/responsive-web-design-basics/)

Remember to:
- Test all changes in multiple browsers
- Keep backups before making significant changes
- Maintain consistent styling throughout the page
- Validate HTML using [W3C Validator](https://validator.w3.org/)