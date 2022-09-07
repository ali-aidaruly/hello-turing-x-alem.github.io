<template>
  <v-app>
    <section id="main">
      <div class="animation-container">
        <div class="animation-block"></div>
      </div>
      <div class="container px-0 px-sm-5 px-md-16">
        <v-sheet color="transparent" class="container__title pixel-font">
          <h1 style="font-size: 48px;">Hello, <br /> Turing x Alem!</h1>
          <h3 style="font-size: 18.72px">Building progressive community</h3>
        </v-sheet>
        <div class="container__content">
          <div class="bold py-5" style="font-size: 18.72px">
            Full heart mentorship that works
          </div>
          <BenefitsList />
          <div class="p-relative d-flex justify-center pt-2">
            <v-btn color="#573b49" class="text-white text-none px-3" height="45" href="https://docs.google.com/forms/d/e/1FAIpQLScwHYFCEfZ6ylEO4Ny48Xog7ftepJHUqk8cnYsF0kG2V990bQ/viewform">
              Apply now 🎉
            </v-btn>
          </div>
        </div>
      </div>
      <footer>
        Hello, Turing x Alem! © 2022, Nur-Sultan
      </footer>
    </section>
  </v-app>
</template>

<script>
import BenefitsList from './components/BenefitsList.vue'

export default {
  name: 'App',
  components: {
    BenefitsList,
  },
  methods: {
    redirectToForm() {
      window.location.href = 'https://docs.google.com/forms/d/e/1FAIpQLScwHYFCEfZ6ylEO4Ny48Xog7ftepJHUqk8cnYsF0kG2V990bQ/viewform'
    }
  }
}
</script>

<style>
@import './assets/font.scss';

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.pixel-font {
  font-family: Joystix;
}

.regular-font {
  font-family: Arial, Helvetica, sans-serif;
}

.bold {
  font-weight: bolder;
}

body {
  max-width: 100vw;
  overflow: hidden;
}

#main {
  padding: 250px 10px 100px;
  color: #573b49;
  min-height: 100vh;
  max-width: 100vw;
  overflow: hidden;
  background-color: #FFFA37;
  display: flex;
  align-items: center;
  flex-direction: column;

}

.container {
  line-height: 1.2;
  max-width: 800px;
}

footer {
  position: absolute;
  bottom: 10px;
  font-weight: bold;
  color: rgba(0, 0, 0, 0.2);
}

@keyframes animate {
  to {
    transform: translateX(-200px);
  }
}

.animation-container {
  width: 100vw;
}

.animation-block {
  transform: translateX(100vw);
  top: 0;
  position: absolute;
  height: 250px;
  width: 250px;
  flex-direction: column;
  background-image: url(https://hello-turing.github.io/_nuxt/img/turing.8547527.gif);
  background-position: 100%;
  background-repeat: no-repeat;
  background-size: contain;
  animation: animate 25s linear infinite;
}
</style>
