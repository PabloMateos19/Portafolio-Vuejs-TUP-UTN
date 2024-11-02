<script setup>
//ESTO ES TODO JS (POR LO QUE PARA COMENTAR SE USA //)
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import EducacionG from './components/EducacionG.vue';
import ExperienciaComponente from './components/ExperienciaComponente.vue';
import ProyectosG from './components/ProyectosG.vue';
import HabilidadesG from './components/HabilidadesG.vue';
import InteresesG from './components/InteresesG.vue';
</script>

<template>
  <!-- ESTO ES HTML-->
      <header id="top">
            <!-- Barra de navegacion-->
          <NavBar />
             <!-- Componente Datos Personales-->   
          <DatosPersonales />         
      </header>
      <main>
        <section id="educacion"><h2>Educación - Cursos</h2>
        <EducacionG/>
        </section>
        <section id="experiencia"><h2>Experiencia</h2>
        <ExperienciaComponente />
        </section>
        <section id="proyectos"><h2>Proyectos</h2>
        <ProyectosG />
        </section>
        <section id="habilidades"><h2>Habilidades</h2>
        <HabilidadesG />
        </section>
        <section id="intereses"><h2>Intereses</h2>
        <InteresesG />
        </section>
      </main>
      <footer>
        <a href="#top">Inicio</a>
        <p>© 2024 Mateos Pablo - Portafolio web - UTN FRSR</p>
    </footer>
</template>

<style scoped>
footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2rem;
    font-size: 1.3rem;
}
</style>
