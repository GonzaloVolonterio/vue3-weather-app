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


AXIOS 

```
ejemplo de cómo podrías implementar solicitudes HTTP en un componente Vue.js 3 y mostrar los resultados en el template:

<template>
  <div>
    <h2>Usuarios</h2>
    <ul>
      <li v-for="user in users" :key="user.id">
        {{ user.name }}
      </li>
    </ul>

    <button @click="fetchUsers">Cargar Usuarios</button>
  </div>
</template>


<script>
import { ref } from 'vue';
import axios from 'axios';

<script setup>  

    // Estado reactivo para almacenar los usuarios
    const users = ref([]);

    // Función para realizar una solicitud GET y cargar los usuarios

    const fetchUsers = () => {
      axios.get('https://jsonplaceholder.typicode.com/users')
        .then(response => {
          users.value = response.data;
        })
        .catch(error => {
          console.error('Error al obtener usuarios:', error);
        });
    };

    // Llamar a fetchUsers cuando el componente se monta
    fetchUsers();

    return {
      users,
      fetchUsers
    };
  }
};

</script>

```
```
como usar axios con las opciones axios.get()

Creamos un estado reactivo users utilizando ref() para almacenar los usuarios obtenidos de la API.
Definimos una función fetchUsers que utiliza Axios para realizar una solicitud GET y obtener los usuarios de la API de JSONPlaceholder.
 Cuando se recibe la respuesta, actualizamos el estado users con los datos obtenidos.
En el template, iteramos sobre la lista de usuarios utilizando v-for y mostramos el nombre de cada usuario en una lista <ul>.
También agregamos un botón que, al hacer clic, llama a la función fetchUsers para cargar los usuarios nuevamente.

import axios from 'axios';

// Realizar una solicitud GET para obtener todos los usuarios

axios.get('https://jsonplaceholder.typicode.com/users')
  .then(response => {
    console.log('Usuarios:', response.data);
  })
  .catch(error => {
    console.error('Error al obtener usuarios:', error);
  });
axios.post():



// Datos del nuevo usuario a enviar
const newUser = {
  name: 'John Doe',
  email: 'john@example.com'
};


// Realizar una solicitud POST para crear un nuevo usuario
axios.post('https://jsonplaceholder.typicode.com/users', newUser)
  .then(response => {
    console.log('Nuevo usuario creado:', response.data);
  })
  .catch(error => {
    console.error('Error al crear nuevo usuario:', error);
  });
axios.put():
javascript
Copiar código
import axios from 'axios';


// Datos actualizados del usuario
const updatedUserData = {
  name: 'John Doe (Updated)',
  email: 'john_updated@example.com'
};


// ID del usuario que se actualizará
const userId = 1;


// Realizar una solicitud PUT para actualizar un usuario existente
axios.put(`https://jsonplaceholder.typicode.com/users/${userId}`, updatedUserData)
  .then(response => {
    console.log('Usuario actualizado:', response.data);
  })
  .catch(error => {
    console.error('Error al actualizar usuario:', error);
  });
axios.patch():
javascript
Copiar código
import axios from 'axios';


// Datos parciales actualizados del usuario
const partialUserData = {
  name: 'Jane Doe (Patched)'
};

// ID del usuario que se actualizará parcialmente
const userId = 1;


// Realizar una solicitud PATCH para actualizar parcialmente un usuario existente
axios.patch(`https://jsonplaceholder.typicode.com/users/${userId}`, partialUserData)
  .then(response => {
    console.log('Usuario actualizado parcialmente:', response.data);
  })
  .catch(error => {
    console.error('Error al actualizar parcialmente el usuario:', error);
  });
axios.delete():
javascript
Copiar código
import axios from 'axios';


// ID del usuario que se eliminará
const userId = 1;

// Realizar una solicitud DELETE para eliminar un usuario existente
axios.delete(`https://jsonplaceholder.typicode.com/users/${userId}`)
  .then(response => {
    console.log('Usuario eliminado:', response.data);
  })
  .catch(error => {
    console.error('Error al eliminar usuario:', error);
  });

```


