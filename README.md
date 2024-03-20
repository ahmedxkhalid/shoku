# Shouk Pet Store

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules and Tailwind Css

# TailwindCss config

Install tailwindcss by using tailwind-cli or by using npm/npx command line

```bash
npm i -D tailwindcss
npx tailwindcss init --all
```
Or install tailwind-cli global to use it any time and use the same config
```bash
npm i -g tailwindcss
tailwindcss init --all
```
So now we have `tailwind.config.js` now we need to add content wich the path of index at the all type of fill tailwind will use

```js
/** @type {import('tailwindcss').Config} */
export default {
  content: [ 
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx,html}",
  ],
  presets: [],
  darkMode: 'media', // or 'class'
  theme: {
    accentColor: ({ theme }) => (
      {
      ...theme('colors'),
      auto: 'auto',
    }
    ),
  }  
}
```

# Postcss Config

```js
export default {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },}
```

So after we make config for the website we should add `@tilwinds` decoration in css to loadit in css make this congif in your `index.css`

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
<center><h1>Happy Hack :) </h1></center>