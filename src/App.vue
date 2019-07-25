<template>
  <div id="app">
    <Header></Header>
    <Main></Main>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "app",
  components: {
    Header,
    Main,
    Footer
  }
};
</script>

<style lang="scss">
@import "./scss/abstracts.scss";

:root {
  --primary-font: "Nunito", sans-serif;
  --secondary-font: "Open Sans", sans-serif;
  --sm: 1.5rem;
  --md: 2rem;
  --lg: 3rem;
  --xl: 4rem;
  --primary-color: #222f3e;
  --secondary-color: #8395a7;
  --light-blue: #48dbfb;
  --mid-blue: #54a0ff;
  --dark-blue: #0984e3;
  --green: #1dd1a1;
  --yellow: #f9ca24;
  --gradient: linear-gradient(to bottom right, #48dafbb0, #0985e398, #54a1ff9b);
}
*,
*::before,
*::after {
  padding: 0;
  margin: 0;
  box-sizing: inherit;
}
html {
  font-size: 62.5%; // 1rem = 10px
  box-sizing: border-box;
  @include respond(big-desktop) {
    font-size: 80%;
  }
  @include respond(tab-land) {
    font-size: 70%;
  }
  @include respond(tab-port) {
    font-size: 60%;
  }
  @include respond(phone) {
    font-size: 50%;
  }
}
body {
  font-family: var(--secondary-font);
  background: var(--gradient) no-repeat;
  color: var(--primary-color);
}
#app {
  width: 70%;
  margin: 8em auto;
  display: grid;
  grid-template-rows: 20em minmax(80em, min-content) 30em;
  box-shadow: 0 0 4em 1em #8395a7a9;
  background-color: rgba(255, 255, 255, 0.829);
}

ul {
  list-style: none;
}
a {
  text-decoration: none;
  font-size: var(--sm);
  color: inherit;
  cursor: pointer;
}
</style>
