<template>
  <div class="wrapper">
    <PageHeader />
    <router-view />
    <PageFooter />
  </div>
</template>

<script>
import PageHeader from "@/components/PageHeader.vue";
import PageFooter from "@/components/PageFooter.vue";
export default {
  name: "Home",
  components: {
    PageHeader,
    PageFooter
  }
};
</script>

<style lang="scss">
@import "@/assets/styles/style.scss";
</style>
