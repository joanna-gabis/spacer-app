<template>
  <div v-for='item in results'>
    <p> {{ item.links[0].href }} </p>
  </div>
</template>
<script>
  export default {
    name: 'Item',

  }

</script>
<style>

</style>
