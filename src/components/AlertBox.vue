<template>
  <div>
    <p>{{ anman }}</p>
    <span>{{ state.count }}</span>
    <button @click="cntPlus">Increment count</button>
  </div>
</template>

<script>
import { reactive, ref } from 'vue';
export default {
  props: {
    anman: {
      type: String,
      default: '',
    },
  },
  setup(props) {
    const state = reactive({
      count: 0,
    });

    const cntPlus = () => {
      console.log(props.anman);
      state.count++;
    };

    return {
      state,
      cntPlus,
    };
  },
};
</script>

<style>
</style>