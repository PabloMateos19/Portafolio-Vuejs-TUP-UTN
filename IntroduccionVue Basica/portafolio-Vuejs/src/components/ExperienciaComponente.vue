<script setup>
import icono1 from '/src/assets/teodolito.svg';
import icono2 from '/src/assets/mapa.svg';
import icono3 from '/src/assets/autodesk.svg';
import icono4 from '/src/assets/estacion.svg';
import icono5 from '/src/assets/compas.svg';

import { ref } from 'vue';
const titulo = 'Encargado de Oficina Técnica';
const fecha = 'Desde Enero 2019 / Actualidad';
const experiencias = ref([
    { id: 1, src: icono1, parrafo: 'Coordinar y supervisar los proyectos de levantamiento topográfico, cartografía y georreferenciación. Asegurar que los proyectos cumplan con las especificaciones técnicas y los plazos establecidos.' },
    { id: 2, src: icono2, parrafo: 'Planificar y asignar recursos (personal, equipos, software) para cada proyecto. Optimizar el uso de recursos y gestionar el presupuesto para maximizar la eficiencia y minimizar costos.' },
    { id: 3, src: icono3, parrafo: 'Utilizar software especializado como AutoCAD Civil 3D y GIS para la creación y edición de planos topográficos.' },
    { id: 4, src: icono4, parrafo: 'Dirigir y coordinar el equipo de topógrafos, delineantes y técnicos, asegurando una comunicación eficaz y cumplimiento de los estándares de calidad.' },
    { id: 5, src: icono5, parrafo: 'Brindar asesoría técnica a clientes sobre proyectos de agrimensura, normativas y procesos.' },
]);
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{ titulo.toLocaleUpperCase() }}</h3>
        <p class="fecha">{{ fecha }}</p>
        <ul class="listado">
            <li class="item" v-for="experencia in experiencias" :key="experencia.id">
                <img class="imagen-svg" :src="experencia.src" width="45rem" :alt="experencia.parrafo">
                <p>{{ experencia.parrafo }}</p>
            </li>

            <!-- <li class="item"><img class="imagen-svg" src="/src/assets/ventas.svg" width="45rem" alt="">
                <p>Lideré un equipo de 5 desarrolladores en la creación de una plataforma de comercio electrónico que incrementó las ventas en un 35% durante el primer año.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/ecomerce.svg" width="45rem" alt="">
                <p>Diseñé y desarrollé aplicaciones web utilizando Node.js, React y MongoDB, logrando reducir el tiempo de carga de las páginas en un 50%.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/configuracion.svg" width="45rem" alt="">
                <p>Implementé soluciones de autenticación y autorización, mejorando la seguridad del sitio web y reduciendo los intentos de acceso no autorizado en un 20%.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/uiux.svg" width="45rem" alt="">
                <p>Colaboré con diseñadores de UX/UI para crear interfaces de usuario atractivas y fáciles de usar, aumentando la satisfacción del cliente en un 15%.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/watch.svg" width="45rem" alt="">
                <p>Automaticé procesos de despliegue continuo utilizando Jenkins y Docker, reduciendo los tiempos de despliegue en un 40%.</p>
            </li> -->
        </ul>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: rgb(28, 41, 52);
    border-radius: 15px;
}

.titulo {
    font-size: 1.5rem;
    color: coral;
}

.fecha {
    font-size: 1rem;
    color: burlywood;
    margin-bottom: 1rem;
}

.listado {
    display: flex;
    flex-direction: column;
}

.item {
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
</style>