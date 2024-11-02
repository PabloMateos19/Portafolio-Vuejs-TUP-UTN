<script setup>
import linkedin from '/src/assets/linkedin_icon.svg';
import facebook from '/src/assets/facebook_icon.svg';
import github from '/src/assets/github_icon.svg';
import cv from '/src/assets/curriculum_icon.svg';

const title = 'Pablo Mateos';
const descripcion = 'Tecnico Universitario en Programación - UTN FRSR';
const residencia = 'San Rafael, Mendoza, Argentina';
const presentacion = 'Bienvenido a mi portafolio de proyectos. Tengo una pasión por la tecnología y el desarrollo de software. Actualmente estoy ampliando mis conocimientos en lenguajes como Python, JavaScript y Java, y estoy emocionado por explorar más en el mundo de la programacion.';
const redesSociales = [
    {id: 1, name: 'linkedin', src: linkedin, url: 'https://www.linkedin.com/in/pablo-mateos-23a883251/'},
    {id: 2, name: 'facebook', src: facebook, url: 'https://www.facebook.com/pablo.mateos/'},
    {id: 3, name: 'github', src: github, url: 'https://github.com/PabloMateos19'},
    {id: 4, name: 'curriculum', src: cv, url: ''},
];
const telefono ='+54 9 2604-338891';
</script>

<template>
    <section class="datos-personales">
        <div class="card">
            <h1>{{title}}</h1>
            <h2>{{descripcion}}</h2>
            <p>{{ presentacion }}</p>
            <ul class="container-lista">
                <li v-for="red in redesSociales" :key="red.id">
                    <a :href="red.url"><img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name"></a>
                </li>
            </ul>
            <h3> ☎ Mi Teléfono personal: {{ telefono }}</h3>
            <h4>{{ residencia }}</h4>
        </div>
    </section>

</template>

<style scoped>
h1 {
    font-size: 2.5rem;
    color:rgb(161, 161, 161) ;
}
h2{
    color:rgb(161, 161, 161)
}
h4{
    color:rgb(161, 161, 161)
}

p {
    font-size: 1.2rem;
    font-weight: 600;
    margin-bottom: 1rem;
    color: rgb(161, 161, 161);
}

.card {
    background-color: rgb(28, 41, 52);
    border-radius: 10px;
    padding: 10px;
    margin: 10px;
    text-align: center;
}

.container-lista {
    display: flex;
    justify-content: center;
    list-style-type: none;
    padding: 0;
    margin: 0;
    text-align: center;
}

.icon-redsocial {
    align-items: center;
    background-color: aliceblue;
    border-radius: 50%;
    padding: 2px;
    margin: 5px;
    box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}

.icon-redcosial:hover {
    background-color: rgb(28, 41, 52);
    box-shadow: 0 0 5px rgba(251, 249, 249, 0934);
}

h3 {
    font-size: 1.2rem;
    font-weight: 600;
}
</style>