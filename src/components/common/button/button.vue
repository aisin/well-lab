<template>
  <button class="we-button" @click="handleClick"><slot></slot></button>
</template>

<script>
export default {
  // name: 'weButton',
  methods: {
    handleClick (evt) {
      this.$emit('click', evt);
    }
  }
};
</script>

<style scoped>
.we-button {
    display: inline-block;
    line-height: 1;
    white-space: nowrap;
    cursor: pointer;
    background: #fff;
    border: 1px solid #bfcbd9;
    color: #1f2d3d;
    -webkit-appearance: none;
    text-align: center;
    box-sizing: border-box;
    outline: none;
    margin: 0;
    -moz-user-select: none;
    -webkit-user-select: none;
    -ms-user-select: none;
    padding: 10px 15px;
    font-size: 14px;
    border-radius: 4px;
    color: #fff;
    background-color: #20a0ff;
    border-color: #20a0ff;
}
</style>
