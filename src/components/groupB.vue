<template>
  <div class="hello">
    <img
      v-for="image in imagesB"
      :key="image.pathShort"
      :src="image.pathLong"
    />
  </div>
</template>

<script>
export default {
  name: "Group_B",

  data() {
    return {
      imagesB: [],
    };
  },
  mounted() {
    this.importB(require.context("@/assets/images/group_b/", true, /\.png$/));
  },
  methods: {
    importB(r) {
      r.keys().forEach((key) =>
        this.imagesB.push({ pathLong: r(key), pathShort: key })
      );
    },
  },
};
</script>
<style>
</style>
