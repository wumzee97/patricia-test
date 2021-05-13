<template>
  <v-app dark>
    <v-main>
      <v-container fill-height>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer
      :absolute="!fixed" class="text-center" color="#f5f5f5"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }} Patricia Test - Alabi Adewumi</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      fixed: false,
    }
  }
}
</script>
