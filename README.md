# static-tailwind

Building a minimal static web page with Tailwind CSS

(Inspired by [this article](https://vsupalov.com/tailwind-with-static-site/) from Vlasidlav Supalov.)

## Steps

- Create minimal index.html
- Check node: `$ node -v`
- Install npx: `$ npm install -g npx`
- Install tailwind: `npm install -D tailwindcss`
- Create a `main.css`:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
- Create a `tailwind.config.js`:
```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./index.html"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
- Build `output.css`: `npx tailwindcss -i ./main.css -o ./tailslim.css --watch`
- Complete the html file with: `<link href="./tailslim.css" rel="stylesheet">`


