<template>
  <v-app id="inspire">
    <v-app-bar app elevation="0">
      <img class="logo pt-5" :src="require('/src/assets/logo-jr.png')" />
      <v-tabs
        center-active
        right
        background-color="transparent"
        active-class="active-tab"
      >
        <v-tab href="#home">Home</v-tab>
        <v-tab>Acerca de mi</v-tab>
        <v-tab>Portafolio</v-tab>
        <v-tab>Contacto</v-tab>
      </v-tabs>
      TODO:crear la funcionalidad enviar correo electronio
      <v-btn large class="white--text ml-10 boton"
        >Envíame un correo electrónico</v-btn
      >
    </v-app-bar>
    <v-main style="background-color: #f5f5f5">
      <section class="intro-section" id="home">
        <v-row class="align-center px-10" style="height: 690px">
          <v-col lg="6" cols="6" class="pa-6 font-weight-bold py-16">
            <h2 class="display-3">
              Programador <span class="blue--text">FullStack</span> En
              <span class="orange--text">Javascript</span>
            </h2>
            <v-subheader
              >Hola soy Jorge, me enfoco en programar con pasion y creatividad
            </v-subheader>
            <br />
            <br />
            <v-btn
              large
              elevation="5"
              class="white--text mt-10 ml-10 px-10 py-5 boton"
              >Contacto
            </v-btn>
            <v-row class="mt-16">
              <v-chip class="px-4 ma-3" color="primary">
                <v-icon left size="20">mdi-facebook</v-icon>
                Facebook
              </v-chip>
              <v-chip class="px-4 ma-3 white--text" color="#01ff56">
                <v-icon left size="20">mdi-whatsapp</v-icon>
                Whatsapp
              </v-chip>
              <v-chip class="px-4 ma-3" color="info">
                <v-icon left size="20">mdi-linkedin</v-icon>
                Linkedin
              </v-chip>
              <v-chip class="px-4 ma-3" color="dark">
                <v-icon left size="20">mdi-github</v-icon>
                Github
              </v-chip>
            </v-row>
          </v-col>
          <v-col lg="6" cols="6">
            TODO:FOTO DE PERFIL
            <v-img></v-img>
          </v-col>
        </v-row>
      </section>
      <section class="about-me" id="about">
        <v-img class="pa-10 color" height="600">
          <v-row justify="center" class="align-center">
            <v-col lg="6" cols="6">
              <v-card
                class="text-center pa-6 rounded-lg"
                color="#e1e0e0c9"
                elevation="6"
              >
                <v-card-subtitle class="">SOBRE MI </v-card-subtitle>
                <h2 class="display-1 font-weight-regular">
                  Full Stack Developer apasionado por la programación, con ganas
                  de seguir creciendo en el área TI y poner en practica nuevas
                  tecnologías.
                </h2>
                <v-btn
                  large
                  elevation="5"
                  class="white--text mt-10 px-10 py-5 boton"
                  >Descargar cv
                  <v-icon>mdi-download</v-icon>
                </v-btn>
              </v-card>
            </v-col>
            <v-col lg="6" cols="6">
              <v-card class="pa-1 rounded-lg" color="#e1e0e0c9" elevation="4">
                <div class="py-1" v-for="(item, index) in items" :key="index">
                  <label>{{ item.title }}</label>

                  <v-progress-linear
                    :color="item.color"
                    height="4"
                    :value="item.value"
                    :icon="item.icon"
                  ></v-progress-linear>
                  <v-icon small class="green--text">mdi-check</v-icon>
                </div>
              </v-card>
            </v-col>
          </v-row>
        </v-img>
      </section>
      <section class="educaion py-6">
        <v-container>
          <h4 class="display-2 text-center">Educacion</h4>
          <v-row class="py-8">
            <v-col cols="12" lg="6">
              <v-card class="pa-6 rounded-xl" elevation="5">
                <div class="d-flex align-center justify-space-between">
                  <div class="">
                    <h2>FullStack Javascript</h2>
                    <span> Noviembre 2020 </span>
                  </div>
                  <a class="blue--text">
                    Desafio latam
                    <v-icon color="white"
                      >https://desafiolatam.com/chile/full-stack-javascript/?utm_source=google&utm_medium=search&utm_campaign=full_stack_javascript_agosto_2021&utm_content=empleo&utm_term=programador%20full%20stack%20que%20es&utm_campaign=full_stack_javascript_agosto_2021&utm_source=adwords&utm_medium=ppc&hsa_acc=1239562006&hsa_cam=13072221065&hsa_grp=125869136127&hsa_ad=570234668858&hsa_src=g&hsa_tgt=kwd-832495968719&hsa_kw=programador%20full%20stack%20que%20es&hsa_mt=b&hsa_net=adwords&hsa_ver=3&gclid=Cj0KCQiAraSPBhDuARIsAM3Js4oHyTBtaLbEPU_MbK_Ttt2mXS6_FF3ut8NAFNs0d5Q71srg-rl3HIoaAiZfEALw_wcB</v-icon
                    ></a
                  >
                </div>
                <v-card-text>
                  Competencias para el Desarollo web Html, Css, Bootstrap,
                  programación con Javascript,manejo de base de datos con
                  Posgrest SQL, Node.js ,Framework Express, api rest ,
                  Handelbars,
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" lg="6">
              <v-card class="pa-6 rounded-xl" elevation="5">
                <div class="d-flex align-center justify-space-between">
                  <div class="">
                    <h2>Hoteleria AIEP</h2>
                    <span>Marzo 2015-2017 </span>
                  </div>
                  <a class="blue--text">
                    AIEP
                    <v-icon color="white">mdi-link</v-icon>
                  </a>
                </div>
                <v-card-text>
                  competencias para administrar las operaciones que dan origen a
                  los servicios de hotelería y resorts, de acuerdo a los
                  estándares de la industria nacional e internacional y a la
                  legislación vigente, en un enfoque de calidad y servicio al
                  cliente, identificando, además, la responsabilidad social y
                  las soluciones sostenibles para los impactos ambientales de
                  dichas operaciones
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </section>
      <section class="experiance color py-6">
        <v-container>
          <h4 class="display-2 text-center">Experiencia</h4>
          <v-timeline>
            <v-timeline-item
              v-for="(exper, index) in experience"
              :key="index"
              :color="index % 2 === 0 ? 'boton' : 'color2'"
            >
              <v-card class="rounded-xl">
                <v-card-title :color="index % 2 === 0 ? 'boton' : 'color2'">
                  {{ exper.title }}
                </v-card-title>
                <v-card-text>
                  <b>{{ exper.date }}</b
                  ><br />
                  <b>@{{ exper.institute }}</b
                  ><br />
                  {{ exper.decription }}
                </v-card-text>
              </v-card>
            </v-timeline-item>
          </v-timeline>
        </v-container>
      </section>
      <section class="portfolio">
        <h4 class="display-2 text-center">Portafolio</h4>
        <v-slide-group class="pa-4" active-class="success" show-arrows>
          <v-slide-item v-for="(slider, index) in sliders" :key="index">
            <v-card height="250" width="250" class="mx-2">
              <img height="100%" width="100%" :src="slider" alt="" />
            </v-card>
          </v-slide-item>
        </v-slide-group>
      </section>
      <section class="contact-us pt-10 color">
        <v-container>
          <h4 class="display-1 text-center mb-5">
            Estoy disponible para trabajar con ustedes y sus proyectos
          </h4>
          <v-divider />
          <br />
          <v-row>
            <v-col cols="12" lg="6">
              <v-card-title></v-card-title>
              <v-form>
                <v-text-field label="Nombre" />
                <v-text-field label="Email" />
                <v-text-field label="Motivo" />
                <v-textarea label="Mensaje" />
                <v-btn large  class="white--text boton"
                  >Enviar mensaje
                </v-btn>
              </v-form>
            </v-col>
            <v-col cols="12" lg="3" offset="2">
              <v-card-title>CONTACTO</v-card-title>
              <v-card-text>
                Santiago,Chile<br />
                +56954247771 <br />
                jorgerioschile@gmail.com <br />
              </v-card-text>
              <v-card-actions>
                <v-btn
                  large
                  elevation="5"
                  class="white--text mt-10 px-10 py-5 boton"
                  >Descargar cv
                  <v-icon>mdi-download</v-icon>
                </v-btn>
              </v-card-actions>
            </v-col>
          </v-row>
        </v-container>
        <v-footer class="mt-4 color2">
          <v-col class="text-center" cols="12">
            <img class="logo pt-5" :src="require('/src/assets/logo-jr.png')" />
          </v-col>
        </v-footer>
      </section>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    drawer: null,
    items: [
      { title: "HTML", value: 70, color: "pink" },
      { title: "CSS", value: 70, color: "deep-orange" },
      { title: "Javascript", value: 70, color: "light-green" },
      { title: "Vuejs", value: 60, color: "blue" },
      { title: "Vuetify", value: 60, color: "black" },
      { title: "Node", value: 70, color: "red" },
      { title: "Express", value: 70, color: "purple" },
      { title: "Postgres", value: 60, color: "success" },
      { title: "React", value: 30, color: "indigo" },
    ],
    experience: [
      {
        title: "Internship trainee Dlab",
        date: "Diciembre 2021 - Present",
        institute: "Latam",
        decription:
          "Proin laoreet elementum ligula, ac tincidunt lorem accumsan nec. Fusce eget urna ante. Donec massa velit, varius a accumsan ac, tempor iaculis massa. Sed placerat justo sed libero varius vulputate.",
      },
      {
        title: "Ayudante de aula",
        date: "Noviembre 2021 - Present",
        institute: "Latam",
        decription:
          "Proin laoreet elementum ligula, ac tincidunt lorem accumsan nec. Fusce eget urna ante. Donec massa velit, varius a accumsan ac, tempor iaculis massa. Sed placerat justo sed libero varius vulputate.",
      },
    ],
    //LINK DE PROYECTOS EN GITHUB
    sliders: [
      "https://cdn.searchenginejournal.com/wp-content/uploads/2020/01/which-web-design-platform-is-right-for-you-5e4d59fb941b9-1520x800.png",
      "https://cdn.searchenginejournal.com/wp-content/uploads/2019/12/5-ways-seo-web-design-go-together-5e2945dd5df37.png",
      "https://data.whicdn.com/images/350420216/original.jpg?t=1605047796",
      "https://1zylgb20pxi7mw2sdr8i4a14-wpengine.netdna-ssl.com/wp-content/uploads/2020/01/projectleft.jpg",
      "https://cdn.dribbble.com/users/702789/screenshots/14012516/media/561a8b7e8cbe51c72c18f4ef0dc72676.png?compress=1&resize=400x300",
      "https://cdn.dribbble.com/users/2399102/screenshots/15522177/media/346d890482d929610d316938e7d48629.png?compress=1&resize=400x300",
    ],
  }),
};
</script>
<style>
.logo {
  height: 11rem;
}
.v-tab.active-tab {
  color: #e91e63;
}
.color {
  background: #373b44; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #373b44,
    #4286f4
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #373b44,
    #4286f4
      ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  box-shadow: #232526;
}

.color2 {
  background: #232526; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #414345,
    #232526
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #414345,
    #232526
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

.v-tab.active-tab::before {
  background-color: #4caf50;
}

.boton {
  background: #f12711; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #f5af19,
    #f12711
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #f5af19,
    #f12711
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}
</style>