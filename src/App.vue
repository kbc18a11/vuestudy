<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <BlogPost
    v-for="post in posts"
    :key="post.id"
    :id="post.id"
    :title="post.title"
    @ositayatunani="ositayatu = $event"
    searchText=""
    @searchTextUpdate="searchText = $event"
  />
  <alert-box>aaa</alert-box>
  <p>{{ ositayatu }}</p>
  <p>{{ searchText }}</p>
</template>

<script>
import BlogPost from './components/BlogPost.vue';
import AlertBox from './components/AlertBox.vue';

export default {
  name: 'App',
  components: {
    BlogPost,
    AlertBox,
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
