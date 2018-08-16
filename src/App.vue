<template>
  <div class="app">
    <nav>
      <router-link to='/'>Search</router-link>
      <router-link to='/about'>About</router-link>
    </nav>
    <router-view/>
  </div>
</template>

<style lang="scss" >
  @import url('https://fonts.googleapis.com/css?family=Montserrat:300,400,600,800');
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body {
    font-family: 'Montserrat', sans-serif;
    height: 100vh;
    background-image: url('./assets/heroimage.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 80% 0%;
  }
</style>
