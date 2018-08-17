<template>
  <input
    id='search'
    type="text"
    name='search'
    :value='value'
    @input='handleChange'
  />
</template>
<script>
  export default {
    name: 'SearchInput',
    props: {
      value: {
        type: String,
        required: true,
      },
    },
    methods: {
      handleChange(e) {
        this.$emit('input', e.target.value);
      },
    },
  }
</script>
<style lang="scss" scoped>
  input {
    width: 250px;
    display: flex;
    flex-direction: column;
    margin-top: 50px;
    height: 30px;
    border: 0;
    border-bottom: 1px solid white;
    background: none;
    color: white;
    text-align: center;
    font-size: 18px;
    font-weight: 300;
    transition: box-shadow .3s ease-out;

    &:focus {
      outline: none;
      box-shadow: 0 10px 20px -8px rgba(255, 255, 255, .5);
    }

    @media (min-width: 768px) {
      font-size: 26px;
      width: 500px;
      align-self: center;
    }
    @media (min-width: 1024px) {
      font-weight: 400;
    }
  }
</style>



