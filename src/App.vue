<template>
  <!-- <PostList /> -->
  <!-- <CreatePost /> -->
  <!-- <TemplateRef /> -->
  <!-- <click-counter></click-counter> -->
  <!-- <hover-counter></hover-counter> -->
  <!-- <demo-one></demo-one> -->
  <!-- <demo-two></demo-two> -->
  <!-- <methods></methods> -->
  <!-- <VModel /> -->
  <!-- <Computed /> -->
  <!-- <Watch /> -->
  <ProvideInject />
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import CreatePost from './components/CreatePost.vue';
import PostList from './components/PostList.vue';
import TemplateRef from './components/TemplateRef.vue';
import DemoOne from './components/DemoOne.vue';
import DemoTwo from './components/DemoTwo.vue';
import Methods from './components/Methods.vue';
import VModel from './components/VModel.vue';
import Computed from './components/Computed.vue';
import Watch from './components/Watch.vue';
import ProvideInject from './components/ProvideInject.vue';

// import ClickCounter from './components/ClickCounter.vue';
// import HoverCounter from './components/HoverCounter.vue';

export default {
  name: 'App',
    components: {
      // PostList,
    // CreatePost,
    // TemplateRef,
    // ClickCounter,
    // HoverCounter,
    // DemoOne
    // DemoTwo
    // Methods
    // VModel
    // Computed
    // Watch
    ProvideInject

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
