<template>
  <div class="bg-black">
    <b-container>
      <header-component></header-component>
      <main-content @openModal="openModal"></main-content>
      <footer-component></footer-component>
    </b-container>
    <popup-modal v-if="modalOpened" @closeModal="closeModal" :modalSource="modalSource"></popup-modal>
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainContent from "./components/MainContent.vue";
import FooterComponent from "./components/FooterComponent.vue";
import PopupModal from "./components/PopupModal.vue";

export default {
  name: "app",
  components: {
    HeaderComponent,
    MainContent,
    FooterComponent,
    PopupModal
  },
  data() {
    return {
      modalOpened: false,
      modalSource: null
    };
  },
  mounted() {
    window.addEventListener("click", e =>
      console.log("targetElement: ", e.target)
    );
  },
  methods: {
    openModal(value) {
      this.modalOpened = true;
      this.modalSource = value;
      document.getElementsByTagName("body")[0].classList.add("modal-open");
    },
    closeModal() {
      this.modalOpened = false;
      document.getElementsByTagName("body")[0].classList.remove("modal-open");
    }
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
/* prevent scrolling when modal opened */
body.modal-open {
  overflow: hidden;
}

.bg-black {
  background-color: #0e1414;
}

/* set cursor to img elements */
img {
  cursor: pointer;
}
</style>


