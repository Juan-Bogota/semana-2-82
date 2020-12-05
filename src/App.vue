<template>
  <div id="app">
    <NewsApi></NewsApi>
    <section class="container-fluid" id="team">
      <div class="row justify-content-center mb-5">
        <div class="col mt-5" v-for="(member, index) of team" :key="index">
          <team-card :member="member"></team-card>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import NewsApi from "./components/NewsApi";
import TeamCard from "./components/TeamCard.vue";

export default {
  name: "App",
  components: {
    NewsApi,
    TeamCard,
  },
  data() {
    return {
      team: [
        {
          codigo: 1,
          nombre: "Paola Hormaza",
          descripcion:
            'Contadora Publica de la Ciudad de Pasto, "La programación está inmersa en muchos ámbitos de la contabilidad una razón más para adquirir un nuevo conocimiento"',
          image: "img/paola.PNG",
          rol: "Desarrolladora FrontEnd",
        },
        {
          codigo: 2,
          nombre: "Kevin Figueroa",
          descripcion:
            "Estudiante de la Universidad Tecnológica de Bolívar, en la carrera de ingeniería de sistemas, 18 años, le gusta el mar, los atardeceres y disfruta de una buena película, se caracteriza por ser una persona calmada, paciente y responsable.",
          image: "img/kevin.PNG",
          rol: "Desarrollador FrontEnd",
        },
        {
          codigo: 3,
          nombre: "Christian Gonzales",
          descripcion:
            "Estudiante de Ingeniería de Sistemas en la UNAB, miembro de la Escuela Latinoamericana de Inteligencia Artificial. si lo puedes imaginar lo puedes programar..",
          image: "img/cristian.PNG",
          rol: "Desarrollador BackEnd",
        },
        {
          codigo: 4,
          nombre: "Juan Lopez",
          descripcion:
            "Soy ingeniero Aeronautico, me gusta mucho programacion especialmente en Arduino, y mi hobbie es jugar ajedrez y montar bicicleta",
          image: "img/juan.jpg",
          rol: "Desarrollador BackEnd",
        },
        {
          codigo: 5,
          nombre: "Camilo Ramirez",
          descripcion:
            " Ingeniero en electrónica de la Universidad del Quindio, tengo 25 años, soy de Armenia, Quindio y me gusta practicar deportes y pasear.",
          image: "img/camilo.PNG",
          rol: "Desarrollador BackEnd",
        },
      ],
    };
  },
};
</script>

<style>
</style>
