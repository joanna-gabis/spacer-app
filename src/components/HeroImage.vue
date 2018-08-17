<template>
<div class="heroImage">
</div>
</template>

<script>
  export default {
    name: 'HeroImage',
  }
</script>

<style lang='scss' scoped >
.heroImage {
  background-image: url('../assets/heroimage.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: 80% 0%;
  width: 100%;
  height: 100vh;
  position: fixed;
  z-index: -1;
  top: 0;

  &::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;
    width: 100%;
    height: 100vh;
    background-color: rgba(0,0,0,.3);
  }
}

</style>
