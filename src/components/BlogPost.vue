<template>
  <div class="blog-post">
    <h4>{{ title }}</h4>
    <button @click="$emit('ositayatunani', id)">Enlarge text</button>
  </div>
  <input
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
  />
</template>

<script>
export default {
  name: 'BlogPost',
  props: {
    id: {
      type: Number,
    },
    title: {
      type: String,
      default: '',
    },
    searchText: {
      type: String,
      default: '',
    },
    modelValue: '',
  },
  emits: ['ositayatunani'],
};
</script>

<style>
</style>