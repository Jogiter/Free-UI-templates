<template>
  <div>
    <Header />
    <Banner />
    <Feature1 />
    <Portfolio />
    <Feature2 />
    <C2a1 />
    <PortfolioText />
  </div>
</template>

<script>
export default {
  components: {
    Header: () => import("@/modules/Header"),
    Banner: () => import("@/modules/Banner"),
    Feature1: () => import("@/modules/Feature1"),
    Portfolio: () => import("@/modules/Portfolio"),
    Feature2: () => import("@/modules/Feature2"),
    C2a1: () => import("@/modules/C2a1"),
    PortfolioText: () => import("@/modules/PortfolioText"),
  }
}
</script>

<style>

</style>
