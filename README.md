## npm create vue@latest

## npm install

## npm run format

## npm run dev



# Install Tailwind CSS

```

npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p


CONFIGURACION

AGREGAR EN tailwind.config.js

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



VOY A MAIN.JS Y LE CAMBIO A LA RUTA  ./SRC/ASSET/STYLE.CSS EN VES E MAIN.JS

style.css

@tailwind base;
@tailwind components;
@tailwind utilities;


npm run dev




App.vue

<template>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</template>

```
