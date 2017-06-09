<template>
  <div class="box">
    <we-button @click="func">确定</we-button>
    <div v-if="rendered" v-show="visible" class="alert">
      <p>Alert!</p>
    </div>
  </div>
</template>

<script>
import weButton from './common/button';

export default {
  data () {
    return {
      rendered: true,
      visible: true
    };
  },
  props: {
    modal: {
      default: true
    },
    closeOnClickModal: {
      default: true
    }
  },
  components: {
    weButton
  },
  methods: {
    func () {
      console.log('clicked...');
    }
  }
};
</script>

<style>
.alert {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
</style>
