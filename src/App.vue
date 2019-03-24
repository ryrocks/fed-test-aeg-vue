<template>
  <div class="bg-black min-h-screen">
    <b-container>
      <header-component></header-component>
      <main-content></main-content>
      <footer-component></footer-component>
    </b-container>
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainContent from "./components/MainContent.vue";
import FooterComponent from "./components/FooterComponent.vue";

export default {
  name: "app",
  components: {
    HeaderComponent,
    MainContent,
    FooterComponent
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Open+Sans:300");
/* define custome styles */
body {
  font-family: "Open Sans", sans-serif !important;
  /* set body as flex to fill out the empty gap */
  display: flex; 
  flex-direction: column;
}

.min-h-screen {
  /* min-height: 100vh; */
}

.bg-black {
  background-color: #0e1414;
}
</style>


