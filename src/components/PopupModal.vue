<template>
  <transition name="modal">
    <div class="fixed-top vw-100 vh-100" @click="closeModal">
      <div class="background h-100 bg-dark"></div>
      <div class="w-50" id="modal">
        <img class="mw-100" :src="modalSource.src" :alt="modalSource.alt">
      </div>
    </div>
  </transition>
</template>
<script lang="js">
export default {
    name: 'PopupModal',
    props: ['modalSource'],
    methods: {
        closeModal() {
            this.$emit('closeModal');
        }
    }
}
</script>
<style lang="less" scoped>
// set opacity to background
.background {
  opacity: 0.5;
}

// customize modal
#modal {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

/*
 * The following styles are auto-applied to elements with
 * transition="modal" when their visibility is toggled
 * by Vue.js.
 *
 */

.modal-enter {
  opacity: 0;
}

.modal-leave-active {
  opacity: 0;
}

.modal-enter .modal-container,
.modal-leave-active .modal-container {
  transform: scale(1.1);
}
</style>

