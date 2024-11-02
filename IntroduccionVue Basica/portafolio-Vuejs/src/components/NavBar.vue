<template>
    <nav class="navbar">
                <div class="navbar-menu">
                  <ul>
                    <a v-for="nav in navegacion" :key="nav.nombre" :href="nav.enlace" class="nav-item">{{nav.nombre}}</a>
                  </ul>
                </div>
             </nav>
</template>

<script setup>
import { ref } from 'vue';
const navegacion= ref([
    {id:1, nombre:'Educación', enlace:'#educacion'},
    {id:2, nombre:'Experiencia', enlace:'#experiencia'},
    {id:3, nombre:'Proyectos', enlace:'#proyectos'},
    {id:4, nombre:'Habilidades', enlace:'#habilidades'},
    {id:5, nombre:'Intereses', enlace:'#intereses'},
]);
</script>

<style scoped>
.navbar {
    background-color: var(--vt-c-indigo); /* Establece el color de fondo usando una variable CSS */
    color: rgb(161, 161, 161); /* Establece el color del texto en blanco */
    padding: 0.5rem 1rem;
    align-items: center;
}
.navbar-item {
    color: rgb(161, 161, 161)f; /* Establece el color del texto en blanco */
    text-decoration: none;
    margin-right: 1rem;
}
.navbar-menu {
    display: flex;
    justify-content: flex-end;
}
.nav-list{
    list-style: none;
}
a{
    border: 1px solid;
    border-color: hsla(160, 100%, 37%, 0.2);
    border-radius: 5px; 
    text-decoration: none; /*Elimina el subrayado de los enlaces y elementos con clase "green*/
    transition: 0.4s; /*Añade una transicion suave para los cambios de estilo*/
    padding: 5px; /*Añade padding alrededor del contenido*/
}
a:hover{
    background-color: hsla(160, 83%, 50%, 0.637); /*Cambia el color de fondo al pasar el mouse sobre un enlace*/
}

@media (max-width: 768px) {
    .navbar-menu {
        display: flex;
        justify-content: flex-end;
        width: 100%;
    }
}

</style>