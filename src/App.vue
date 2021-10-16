<template>
  <div id="app">

    <top-banner v-bind:idCarousel="['carousel1']" ></top-banner>

    <div class="container-fluid">

<!-- aquí se deberían cargar 4 películas que simulan las 4 noticias pero el hook no es el correcto -->
          <section-api></section-api>
        </div>

<!-- Esta es la tarjeta de miembros que nos piden pero al parecer estamos enviando las props de mala manera o con un nombre no correcro -->
    <div class="container-fluid">
      <div class="row justify-content-center mb-5">
        <div class="col mt-5" v-for="(item, index) of team" :key="index">
          <team-card :member="item"></team-card>
        </div>
      </div>
    </div>

    <page-footer></page-footer>
    <!-- <h1>{{ title }}</h1> -->
  </div>
</template>

<script>
import PageFooter from "./components/PageFooter.vue";
import TeamCard from "./components/TeamCard.vue";
import SectionApi from "./components/SectionApi.vue";
import TopBanner from './components/TopBanner.vue';

export default {
  name: "App",
  components: {
    PageFooter,
    TeamCard,
    SectionApi,
    TopBanner,
  },
  data(){
    return {
      title: "Vivo dentro de VUE",
      carousel1 : 'carousel1',
      // Esta es la definición del objeto team, el objeto contiene la info de cada miembro del equipo
      // Se esta enviando correctamente en el ciclo v-for pero las pruebas fallan
      // Al parecer tenemos un problema con la definición de los nombres de los atributos
      team: [
        {
          codigo: 1,
          nombre: "Zona de servicio de parqueo 1",
          descripcion:
            "1. Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolore omnis, laudantium tempore, provident corporis iure ex libero repellendus accusamus accusantium at voluptate excepturi voluptatem quis, illo modi exercitationem error consequatur.",
          rol: "Nivel A",
          imagen: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSgtPpg7WHk63QI69pt6A4z2U6HSOGRb-RuKg&usqp=CAU",
        },
        {
          codigo: 2,
          nombre: "Zona de servicio de parqueo 2",
          descripcion:
            "2. Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolore omnis, laudantium tempore, provident corporis iure ex libero repellendus accusamus accusantium at voluptate excepturi voluptatem quis, illo modi exercitationem error consequatur.",
          rol: "Nivel B",
          imagen: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRee0WKgegl2XEQ6nV9WP3LIlpOnW8nQ3eeoQ&usqp=CAU",
        },
        {
          codigo: 3,
          nombre: "Zona de servicio de parqueo 3",
          descripcion:
            "3. Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolore omnis, laudantium tempore, provident corporis iure ex libero repellendus accusamus accusantium at voluptate excepturi voluptatem quis, illo modi exercitationem error consequatur.",
          rol: "Nivel C",
          imagen: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSb6FuNzWH4jJxDJ5uebylhdqstNrcV8pOXyQ&usqp=CAU",
        },
        {
          codigo: 4,
          nombre: "Zona de servicio de parqueo 4",
          descripcion:
            "4. Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolore omnis, laudantium tempore, provident corporis iure ex libero repellendus accusamus accusantium at voluptate excepturi voluptatem quis, illo modi exercitationem error consequatur.",
          rol: "Nivel D",
          imagen: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS4qBi2L4N5_p0wztc_fFJOycQ9JdCOGiN93w&usqp=CAU",
        },
        
      ],
    };
  },
};
</script>