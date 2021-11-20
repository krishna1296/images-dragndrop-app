<template>
  <div class="hello">
    <img
      v-for="image in imagesA"
      :key="image.pathShort"
      :src="image.pathLong"
    />
  </div>
</template>

<script>
export default {
  name: "Group_A",

  data() {
    return {
      imagesA: [],
    };
  },
  mounted() {
    this.importA(require.context("@/assets/images/group_a/", true, /\.png$/));
  },
  methods: {
    importA(r) {
      r.keys().forEach((key) =>
        this.imagesA.push({ pathLong: r(key), pathShort: key })
      );
    },
  },
};
</script>
<style>
</style>
