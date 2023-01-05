# CSS in the App Directory

## Before
In the pages directory, global stylesheets are restricted to only pages/_app.js. 

## After
With the app directory, this restriction has been lifted. Global styles can be added to any layout, page, or component.

## Other notes
CSS-in-JS libraries which require runtime JavaScript are not currently supported in Server Components. Using CSS-in-JS with newer React features like Server Components and Streaming requires library authors to support the latest version of React, including concurrent rendering.

If you want to style Server Components, we recommend using either:
- CSS Modules
- Other solutions that output CSS files, like PostCSS or Tailwind CSS.

## Example
```jsx
// These styles apply to every route in the application
import './global.css';

export default function RootLayout({ children }: {
  children: React.ReactNode;
}) {
  return (
    <html lang="en">
      <body>{children}</body>
    </html>
  );
}

