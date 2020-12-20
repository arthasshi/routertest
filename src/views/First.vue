<template>
  <div>
    我是朋友圈列表
    <!-- <router-link to="/first/child1">child1</router-link>｜
    <router-link to="/first/child2">child2</router-link>-->
    <!-- <div @click="gotoPage('/first/child1')">child1</div>
    <div @click="gotoPage('/first/child2')">child2</div>-->
    <div @click="gotoPage('child1')">child1</div>
    <div @click="gotoPage('child2')">child2</div>
    <div @click="gobackPage">back</div>
    <div @click>照相机</div>
    <router-view />
  </div>
</template>

<script>
//http://www.baidu.com/1/23/111 params
//http://www.baidu.com?name=123 query
export default {
  beforeCreate() {
    console.log("我是beforecreate");
  },
  created() {
    console.log("我是created");
  },
  beforeMount() {
    console.log("我是beforemount");
  },
  mounted() {
    console.log("我是mounted");
  },
  beforeUpdate() {
    console.log("我是beforeupdate");
  },
  updated() {
    console.log("updated");
  },
  beforeDestroy() {
    console.log("我是beforedestory");
  },
  destroyed() {
    console.log("destroyed");
  },
  methods: {
    gotoPage(str) {
      const userId = "123";
      this.$router.push({ name: str, params: { userId } });
      //   this.$router.push({ path: str, query: { userId: "123" } });
    },
    gobackPage() {
      this.$router.go(-1);
    }
  }
};
</script>

<style lang="scss" scoped>
</style>