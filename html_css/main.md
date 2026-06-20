# HTML & CSS

## References

### Glossaries

- **[Small and Concise HTML Reference](https://madebymike.github.io/html5-periodic-table/#shadow)**

- **[Full HTML Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements)**

- **[Small and Concise CSS Reference](https://cssreference.io/)**

- **[Full CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)**

- **[Emmet Cheat Sheet](https://docs.emmet.io/cheat-sheet/)**

### Resources

- **[SVG Repository](https://www.svgrepo.com/)**

- **[CSS & SVG Repository](https://css.gg)**

- **[Google Fonts](https://fonts.google.com/)**

### Elements

- **[UI Elements: CSS & Tailwind](https://uiverse.io/elements)**

- **[Codepen: Trending Elements](https://codepen.io/trending)**

## Tools

- **[Can I use?](https://caniuse.com/?search=input)**: Used to check whether any HTML, CSS, or JavaScript feature is supported by a given browser and to what extent. Very useful when working with newer functionalities.

- **[Lighthouse](https://developer.chrome.com/docs/lighthouse/)**: Used to scan a website and analyze aspects like performance, accessibility, and SEO.

- **[Default CSS Styles]()**

### CSS

- **[Flexplorer](https://bennettfeely.com/flexplorer/)**: Lets you experiment with Flexbox to learn or review its functionality.

- **[CSS Pie Chart](https://bennettfeely.com/csspiechart/)**: Lets you create a pie chart using CSS only.

- **[CSS Image Effects](https://bennettfeely.com/image-effects/)**: Lets you create image filters using CSS only.

- **[CSS Gradient](https://cssgradient.io/)**: Lets you create and customize CSS gradient patterns.

- **[Autoprefixer CSS](https://autoprefixer.github.io/)**: Automatically adds vendor prefixes to your CSS code.

- **[Typescale](https://typescale.com/)**: Lets you visualize fonts at different styles and sizes, and export them as CSS code.

## Tips & Tricks

### HTML

1. For better readability, follow this attribute order for **HTML** elements:
   1. class
   2. id, name
   3. data-
   4. src, for, type, href, value
   5. title, alt
   6. role, aria-
   7. tabindex
   8. style

2. When validating forms, don't rely solely on the `required` attribute. Implement server-side validation as well for added security.

3. Place `<link>` tags inside the `<head>` section, preferably towards the end. Similarly, place `<script>` tags at the bottom of the `<body>` section.

   ```html
   <!DOCTYPE html>
   <html lang="en">
     <head>
       <meta charset="UTF-8" />
       <meta name="viewport" content="width=device-width, initial-scale=1.0" />
       <title>Document</title>
       <!-- CSS Styles -->
       <link rel="stylesheet" href="styles.css" />
     </head>
     <body>
       <!-- JavaScript Code -->
       <script src="index.js"></script>
     </body>
   </html>
   ```

4. If you use special characters like `>`, `<`, `&`, or `"` in your **HTML**, use their corresponding HTML entities to ensure they render correctly, especially alongside **JavaScript** or **PHP**:

   | Entity   | Symbol |
   | -------- | ------ |
   | `&lt;`   | <      |
   | `&gt;`   | >      |
   | `&amp;`  | &      |
   | `&quot;` | "      |

5. An **HTML** document should only contain one `<h1>` element.

6. Use `<em>` to emphasize text rather than `<i>`. The `<i>` tag is now widely accepted for representing icons.

7. To test your website on your phone, make sure it's connected to the same network as your computer. Run `ipconfig` in the terminal, find the **IPv4 Address**, and enter that IP along with your server's port in your phone's browser (e.g., `192.168.0.230:5500`). If it doesn't work, refer to this video: **[How to test a local website on your phone](https://www.youtube.com/watch?v=uRYHX4EwYYA)**.

### SEO

1. Always provide a meaningful value for the `alt` attribute on images. This improves both accessibility and search engine rankings.

2. Include a canonical URL in the `<head>` section for better search engine indexing:

   ```html
   <link rel="canonical" href="https://example.com/preferred-url-here/" />
   ```

3. Favicon support is limited to desktop browsers by default. To enable favicons on mobile devices, add the following tag to your `<head>` section:

   ```html
   <link rel="apple-touch-icon" href="img/favicon.png" />
   ```

4. Avoid overusing `<div>` tags. Prefer semantic elements like `<main>`, `<section>`, `<article>`, and others for cleaner, more structured markup. This also helps search engines better understand and rank your content.

5. Always include the `lang` attribute on the `<html>` tag. This helps voice synthesis tools determine correct pronunciations and allows translation tools to apply proper grammatical rules.

6. The `<title>` tag should be between 55 and 65 characters, and the `<meta name="description">` tag should not exceed 165 characters for optimal search engine positioning.

### CSS

1. Common breakpoints for device resolutions:

   | Screen Size | Scope                                                                                                 |
   | ----------- | ----------------------------------------------------------------------------------------------------- |
   | 320px       | Small-screen devices, like phones, in portrait mode.                                                  |
   | 480px       | Small-screen devices, like phones, in landscape mode.                                                 |
   | 600px       | Small tablets, like the Amazon Kindle (600×800) and Barnes & Noble Nook (600×1024), in portrait mode. |
   | 768px       | 10-inch tablets like the iPad (768×1024), in portrait mode.                                           |
   | 1024px      | Tablets like the iPad (1024×768) in landscape mode, and some laptops and desktop screens.             |
   | 1200px      | Widescreen displays, mostly laptops and desktops.                                                     |

2. The correct order of link pseudo-classes is:
   1. **:link**
   2. **:hover**
   3. **:active**
   4. **:visited**

3. If a child element has a width set in percentages, the parent will automatically expand to occupy 100% of the available space. Be mindful of this behavior and control it when necessary.

4. To get an overview of the CSS styles used on a website, open DevTools (F12) > More options (three dots at the top) > More tools > CSS Overview.

5. In Visual Studio Code, you can switch between color formats by hovering over a color swatch and clicking the value at the top of the color picker. Each click cycles through the available formats.

6. Recommended CSS declaration order:

   ```css
   .declaration-order {
     /* Positioning */
     position: absolute;
     top: 0;
     right: 0;
     bottom: 0;
     left: 0;
     z-index: 100;

     /* Box model */
     display: flex;
     flex-direction: column;
     justify-content: center;
     align-items: center;
     width: 100px;
     height: 100px;

     /* Typography */
     font:
       normal 14px "Helvetica Neue",
       sans-serif;
     line-height: 1.5;
     color: #333;
     text-align: center;
     text-decoration: underline;

     /* Visual */
     background-color: #f5f5f5;
     border: 1px solid #e5e5e5;
     border-radius: 3px;

     /* Misc */
     opacity: 1;
   }
   ```

7. **BEM (Block-Element-Modifier)** is a naming convention for HTML and CSS classes. Originally developed by Yandex with large codebases and scalability in mind, it serves as a solid foundation for implementing Object-Oriented CSS (OOCSS):

   ```jsx
   // ListingCard.jsx
   function ListingCard() {
     return (
       <article class="ListingCard ListingCard--featured">
         <h1 class="ListingCard__title">Adorable 2BR in the sunny Mission</h1>

         <div class="ListingCard__content">
           <p>Vestibulum id ligula porta felis euismod semper.</p>
         </div>
       </article>
     );
   }
   ```
