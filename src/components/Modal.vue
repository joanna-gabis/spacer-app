<template>
<div class="outerWrapper">
  <div class="innerWrapper">
    <div class="photo">
      <img src='https://static.baza.farpost.ru/v/1501302674422_bulletin'/>
    </div>
    <div class="description">
      <h2 class='title'>Lorem ipsum</h2>
      <p class='description'>Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
      </p>
    </div>
  </div>
  <div class="close" @click='$emit("closeModal")' />
</div>
</template>

<script>
export default {
name: 'Modal',

}
</script>

<style lang='scss' scoped >
.outerWrapper {
  max-width: 100%;
  height: 100%;
  position: fixed;
  top: 0;
  left: 0;
  background: #f6f6ff;
}

.innerWrapper {
  display: flex;
  height: 100%;
  padding: 50px;
  justify-content: enter;
  align-items: center;
  flex-direction: column;

  .photo {
    max-width: 100%;
    height: auto;
    background: black;

    img {
      width: 100%;

    }
  }

  .description {
    color: #333;
  }

}
.close {
    position: absolute;
    right: 30px;
    top: 20px;
    width: 30px;
    height: 30px;
    //padding: 30px;
    cursor: pointer;

    &::before,
    &::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 2px;
      background: black;
      display: block;
      //top: 0;
      //right: 0;
    }
    &::before {
      transform: rotate(45deg);
    }
    &::after {
      transform: rotate(-45deg);
    }
  }
</style>