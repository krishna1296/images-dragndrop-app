<template>
  <div class="hello">
    <img
      v-for="image in imagesC"
      :key="image.pathShort"
      :src="image.pathLong"
    />
  </div>
</template>

<script>
export default {
  name: "Group_C",

  data() {
    return {
      imagesC: [],
    };
  },
  mounted() {
    this.importC(require.context("@/assets/images/group_c/", true, /\.png$/));
  },
  methods: {
    importC(r) {
      r.keys().forEach((key) =>
        this.imagesC.push({ pathLong: r(key), pathShort: key })
      );
    },
  },
};
</script>
<style>
</style>
