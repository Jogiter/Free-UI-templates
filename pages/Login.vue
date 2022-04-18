<template>
  <div>
    <Header />
    <Login />
  </div>
</template>

<script>
export default {
  layout: 'site',
  components: {
    Header: () => import("@/modules/Header"),
    Login: () => import('@/modules/Login')
  },
};
</script>

<style>

</style>
