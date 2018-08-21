<template>
<div class="outerWrapper">
  <div class="innerWrapper">
    <div class="photo">
      <img :src='photo'/>
    </div>
    <div class="description">
      <h2 class='title'>{{ title }} </h2>
      <p class='description'> {{ description }}
      </p>
    </div>
  </div>
  <div class="close" @click='$emit("closeModal")' />
</div>
</template>

<script>
export default {
name: 'Modal',
props: {
  item: {
    type: Object,
    required: true,
  },
},
data() {
  return {
    photo: null,
    title: null,
    description: null,
  }
},
mounted() {
  this.photo = this.item.links[0].href;
  this.title = this.item.data[0].title;
  this.description = this.item.data[0].description.substr(0, 200);
},
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

  @media (min-width: 1024px) {
    max-width: 70%;
    height: 60%;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    margin: auto;
    box-shadow: 0 30px 30px -10px rgba(0,0,0,.3);
  }
}

.innerWrapper {
  display: flex;
  height: 100%;
  padding: 50px;
  justify-content: center;
  align-items: center;
  flex-direction: column;

  @media (min-width: 1024px) {
    flex-direction: row;
  }

  .photo {
    width: 100%;
    height: 100%;
    background: black;

    @media (min-width: 1024px) {
      width: 50%;
      margin-right: 40px;
    }

    img {
      width: 100%;
      height: 100%;
    }
  }

  .description {
    color: #333;
    margin-top: 10px;
  }

  .title {
    color: #1e3d4a;
  }

}
.close {
    position: absolute;
    right: 30px;
    top: 30px;
    width: 30px;
    height: 30px;
    cursor: pointer;

    &::before,
    &::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 2px;
      background: black;
      display: block;
      top: 0;
      right: 0;
    }
    &::before {
      transform: rotate(45deg);
    }
    &::after {
      transform: rotate(-45deg);
    }
  }
</style>