<template>
  <div id="list-rendering">
    <ol>
      <li v-for="todo in todos" :key="todo.text">
        {{ todo.text }}
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
  data() {
    return {
      message: 'Hello Vue.js!',
      seen: false,
      todos: [
        { text: 'Learn JavaScript' },
        { text: 'Learn Vue' },
        { text: 'Build something awesome' },
      ],
    };
  },
  mounted() {},
  methods: {
    reverseMessage() {
      this.message = this.message.split('').reverse().join('');
    },
  },
};
</script>
