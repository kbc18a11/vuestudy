<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <BlogPost
    v-bind:style="{ fontSize: postFontSize + 'em' }"
    v-for="post in posts"
    :key="post.id"
    :id="post.id"
    :title="post.title"
    @ositayatunani="ositayatu = $event"
    v-model="searchText"
  />
  <p>{{ ositayatu }}</p>
  <p>{{ searchText }}</p>
</template>

<script>
import BlogPost from './components/BlogPost.vue';

export default {
  name: 'App',
  components: {
    BlogPost,
  },
  data() {
    return {
      posts: [
        { id: 1, title: 'My journey with Vue' },
        { id: 2, title: 'Blogging with Vue' },
        { id: 3, title: 'Why Vue is so fun' },
      ],
      postFontSize: 1,
      ositayatu: '',
      searchText: '',
    };
  },
};
</script>
