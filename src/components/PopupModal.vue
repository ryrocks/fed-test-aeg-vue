<template>
  <div class="fixed-top vw-100 vh-100" @click="closeModal">
    <div class="background h-100 bg-dark"></div>
    <div class="w-50" id="modal">
      <img class="mw-100" :src="modalSource.src" :alt="modalSource.alt">
    </div>
  </div>
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
</style>

