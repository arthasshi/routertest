<template>
  <div>我是编辑朋友圈页面</div>
</template>

<script>
export default {
  data() {
    return {
      key: ""
    };
  },
  created() {
    console.log(this.$route.params.userId);
  },
  methods: {
    getRouterInfo() {}
  }
};
</script>

<style lang="scss" scoped>
</style>