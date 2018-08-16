<template>
  <div class="wrapper">
    <div class="search">
      <label for='search'>Search</label>
      <input id='search' type="text" name='search' v-model='searchValue' @input='handleInput'>
    </div>
  </div>
</template>

<script>
  const API = 'https://images-api.nasa.gov';
  export default {
    name: 'Search',
    data() {
      return {
        searchValue: '',
      };
    },
    methods: {
      handleInput() {
        console.log(this.searchValue);
      },
    }
  };
</script>

<style lang='scss' scoped>
  .wrapper {
    width: 100%;
    margin: 0;
    padding: 30px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .search {
    width: 300px;
    display: flex;
    flex-direction: column;

    label {
      font-family: Montserrat, sans-serif;
    }
    input {
      height: 30px;
      border: 0;
      border-bottom: 1px solid black;
    }
  }
</style>

