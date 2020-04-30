<template>
  <v-container ref="container">
    <v-btn @click="goTo">goTo</v-btn>
    <div style="background-color:red; height: 500px; width: 100%"></div>
    <div style="background-color:green; height: 500px; width: 100%"></div>
    <div ref="div" style="background-color:blue; height: 500px; width: 100%"></div>
  </v-container>
</template>

<script>
  export default {

    methods: {

      async goTo() {

        const m1 = Date.now()
        await this.$vuetify.goTo(this.$refs.div, { duration: 5000 })
        const m2 = Date.now()
        console.log(m2 - m1)
      }
    }
  }
</script>
