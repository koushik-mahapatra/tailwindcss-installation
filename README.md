# TailwindCSS installation.

## TailwindCSS installation with vite and prettier-plugin.

**To setup tailwind css, run these commands**

- `npm init -y` **This initializes the directory as a NODEJS project**
- `npm install -D tailwindcss postcss  autoprefixer vite` **Installs required packages**
- `npx tailwindcss init -p`

- Create a css file `index.css` link it to `HTML` file and edit with these content :

`@tailwind base;
@tailwind components;
@tailwind utilities;`

- Inside the **tailwind.config.js** file replace **content [],** with ⬇

`/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ['*.{html,js}'],
  theme: {
    extend: {},
  },
  plugins: [],
};`

- Add **“start”: “vite” and “build”: “vite build”** to script in `package.json`

`"scripts": {
    "start": "vite",
    "build": "vite build"
  }`

- to install **prettier** and **prettier-plugin-tailwindcss**

`npm install -D prettier prettier-plugin-tailwindcss`

- add a **.prettierrc** file and these ⬇ to the file

`{
  "plugins": ["prettier-plugin-tailwindcss"]
}`

- Run `npm run start` or `npm start` to start a dev server or `npm start -- --host` to host the server.

- Run `npm build` to build the production code.
