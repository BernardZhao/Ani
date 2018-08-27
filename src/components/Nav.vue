<template>
  <sui-menu inverted id="nav">
    <sui-container>
      <router-link 
        v-for="route in routes"
        :key="route.name"
        tag="sui-menu-item"
        :to="route.path"
        >
        <a>{{route.name}}</a>
      </router-link>

      <sui-menu-menu position="right">
        <a
        is="sui-menu-item"
        :content="'logout'"
        />
      </sui-menu-menu>
    </sui-container>
  </sui-menu>

</template>

<script>
export default {
  computed: {
    routes() {
      return this.$router.options.routes
    }
  }
}
</script>

<style scoped>
#nav {
  margin: 0;
}
</style>