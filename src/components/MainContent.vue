<template>
  <section class="my-5 py-5">
    <!-- Top Block -->
    <div class="row">
      <div class="col-lg-4 col-md-6">
        <img class="mw-100" src="./../assets/1.png" alt="pic-1" @click="openModal">
      </div>
      <div class="col-lg-4 col-md-6 d-flex flex-column justify-content-between">
        <img class="mw-100" src="./../assets/2.png" alt="pic-2" @click="openModal">
        <img class="mw-100" src="./../assets/3.png" alt="pic-3" @click="openModal">
      </div>
      <article class="col-lg-4 col-md-12 text-white font-weight-lighter">
        <h4 class="border-bottom pt-1 pb-3">
          <a href ref="external" target="_blank">ANSWER YOUR BODY'S NEEDS</a>
        </h4>
        <p class="my-4">
          The way ingredients are sourced affects the way we nourish
          our bodies. Author Mark Schatzer believes our body naturally
          develops an appetite for the foods and nutrients it needs to
          be healthy, but that artificial flavourings are getting in the
          way. This can be reversed by focusing on high-quality ingredients
          and being mindful as your appetite guides you to consume according
          to your body’s needs.
        </p>
        <h6 class="text-danger mt-5">BE MINDFUL</h6>
        <p class="mt-3 font-weight-bold">
          Sourcing local or organic food is a good way to start being more
          mindful about what you’re cooking and eating.
        </p>
      </article>
    </div>

    <!-- Bottom Block -->
    <div class="text-white mt-5 py-5">
      <h1 class="text-center py-5">ALL THE LATEDT FROM AEG</h1>
      <div class="row mt-4">
        <div class="col-sm-4 col-12 d-flex flex-column justify-content-between">
          <img
            class="mw-100 border-bottom border-danger border-4"
            src="./../assets/4.png"
            alt="pic-4"
            @click="openModal"
          >
          <article class="py-3 mt-3 flex-grow-1">
            <h6 class="py-2 font-weight-bold">Summer Lunch Menu By Mark Best</h6>
            <p class="font-weight-lighter text-gray font-15">
              AEG ambassador Mark Best’s summer eats are guaranteed to help you
              make the most of the warmer weather and entertaining at home.
            </p>
          </article>
          <div class="d-flex">
            <span class="read-more-bottom">READ MORE</span>
            <span class="flex-grow-1"></span>
          </div>
        </div>
        <div class="col-sm-4 col-12 d-flex flex-column justify-content-between">
          <img
            class="mw-100 border-bottom border-danger border-4"
            src="./../assets/5.png"
            alt="pic-5"
            @click="openModal"
          >
          <article class="py-3 mt-3 flex-grow-1">
            <h6 class="py-2 font-weight-bold">A Traditional Christmas Eve, Mark Best Style</h6>
            <p class="font-weight-lighter text-gray font-15">
              One of Australia’s best chefs and AEG ambassador, Mark Best, shares
              his favourite Christmas Eve menu which is sure to impress your guests.
            </p>
          </article>
          <div class="d-flex">
            <span class="read-more-bottom">READ MORE</span>
            <span class="flex-grow-1"></span>
          </div>
        </div>
        <div class="col-sm-4 col-12 d-flex flex-column justify-content-between">
          <img
            class="mw-100 border-bottom border-danger border-4"
            src="./../assets/6.png"
            alt="pic-6"
            @click="openModal"
          >
          <article class="py-3 mt-3 flex-grow-1">
            <h6 class="py-2 font-weight-bold">Taking Taste Further</h6>
            <p class="font-weight-lighter text-gray font-15">
              This exclusive cookbook gives you all the know-how you need. We’ve
              designed it to make sure you get the most out of our products - and the
              best out of your food.
            </p>
          </article>
          <div class="d-flex">
            <span class="read-more-bottom">READ MORE</span>
            <span class="flex-grow-1"></span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script lang="js">
export default {
    name: 'MainContent',
    methods: {
      openModal(event) {
        this.$emit('openModal', {
          src: event.target.src,
          alt: event.target.alt
        });
      }
    }
}
</script>
<style lang="less" scoped>
// define class for border width
.border-4 {
  border-width: 4px !important;
}

// article color
.text-gray {
  color: #c2c2c2;
}

// article font-size
.font-15 {
  font-size: 15px;
}

// remove default style for a tag
a {
  color: inherit;
  text-decoration: none;
  &:hover {
    color: inherit;
    text-decoration: none;
  }
}

// READMORE border 
.read-more-bottom {
  display: inline-block;
  position: relative;
  &:after {
    content: "";
    display: block;
    margin-top: 5px;
    height: 1px;
    width: 0px;
    background: transparent;
    transition: width 0.5s ease, background-color 0.5s ease;
  }
  &:hover:after {
    width: 100%;
    background: red;
  }
}

// simple effects
img {
  transition: opacity 0.5s ease-in-out;
  &:hover {
    opacity: 0.5;
  }
}
</style>

