<template>
  <div class="blog-post">
    <h4>{{ title }}</h4>
    <button @click="onClickId">Enlarge text</button>
  </div>
  <input :value="searchText" @input="changeText" />
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
  },
  emits: ['ositayatunani', 'searchTextUpdate'],
  computed: {
    onClickId: function (e) {
      this.$emit('ositayatunani', this.id);
    },
    changeText: function (e) {
      console.log(e);
      this.$emit('searchTextUpdate', e.target.value);
    },
  },
};
</script>

<style>
</style>