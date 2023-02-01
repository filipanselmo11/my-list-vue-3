<template>
  <div>
    <h1>My List Vue 3 App</h1>
    <br/>
    <my-list-component></my-list-component>
  </div>
</template>

<script>
import MyListComponent from "./components/MyListComponent.vue";
export default {
  name: "App",
  components: {
    MyListComponent,
  },
};
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
  /* background-color: rgb(0, 0, 0) !important; */
}
</style>
