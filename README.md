##npm create vue@latest

  ##npm install
  ##npm run format
  ##npm run dev



# Install Tailwind CSS

```

npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p


Configure your template paths
Add the paths to all of your template files in your tailwind.config.js file.

tailwind.config.js

/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{vue,js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}



Add the Tailwind directives to your CSS
Add the @tailwind directives for each of Tailwind’s layers to your ./src/asset/style.css file. Creo style.css y borro main.css

voy a main.js y le cambio a la ruta  ./src/asset/style.css 

style.css


@tailwind base;
@tailwind components;
@tailwind utilities;
Start your build process
Run your build process with npm run dev.

Terminal

npm run dev




App.vue

<template>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</template>

```
