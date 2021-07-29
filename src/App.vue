<template>
  <!-- <PostList /> -->
  <!-- <CreatePost /> -->
  <!-- <TemplateRef /> -->
  <!-- <click-counter></click-counter> -->
  <!-- <hover-counter></hover-counter> -->
  <demo-one></demo-one>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import CreatePost from './components/CreatePost.vue';
import PostList from './components/PostList.vue';
import TemplateRef from './components/TemplateRef.vue';
import DemoOne from './components/DemoOne.vue';
// import ClickCounter from './components/ClickCounter.vue';
// import HoverCounter from './components/HoverCounter.vue';

export default {
  name: 'App',
    components: {
        DemoOne
    // PostList,
    // CreatePost,
    // TemplateRef,
    // ClickCounter,
    // HoverCounter,

  },
}
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
