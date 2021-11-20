<template>
  <v-container>
    <v-card>
      <v-tabs v-model="tab" background-color="primary" dark>
        <v-tab v-for="item in items" :key="item.tab">
          {{ item.tab }}
        </v-tab>
      </v-tabs>
      <v-tabs-items v-model="tab">
        <v-tab-item v-for="item in items" :key="item.tab">
          <v-card flat>
            <v-card-text>
              <component v-bind:is="item.content"></component>
            </v-card-text>
          </v-card>
        </v-tab-item>
      </v-tabs-items>
    </v-card>
  </v-container>
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
  data() {
    return {
      tab: null,
      items: [
        { tab: "Group_A", content: "GroupA" },
        { tab: "Group_B", content: "GroupB" },
        { tab: "Group_C", content: "GroupC" },
      ],
    };
  },

  methods: {},
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
