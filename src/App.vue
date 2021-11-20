<template>
  <GroupA />
  <GroupB />
  <GroupC />
</template>

<script>
import GroupA from "./components/groupA.vue";
import GroupB from "./components/groupB.vue";
import GroupC from "./components/groupC.vue";

export default {
  name: "App",
  components: {
    GroupA,
    GroupB,
    GroupC,
  },
};
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
