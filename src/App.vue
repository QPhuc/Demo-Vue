<template>
  <PostList />
  <CreatePost />
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import CreatePost from './components/CreatePost.vue';
import PostList from './components/PostList.vue';

@Options({
  components: {
    PostList,
    CreatePost
    
  },
})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
