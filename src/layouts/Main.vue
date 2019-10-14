<template>
  <div class="container">
    <div class='nav'>
        <v-link href="/emails">Emails</v-link>
        <v-link href="/">Home</v-link>
        <v-link href="/text">Text</v-link>
    </div>

    <slot></slot>
  </div>
</template>

<script>
  import VLink from '../components/VLink.vue'

  export default {
    components: {
      VLink
    }
  }
</script>

<style scoped>
  .nav{
    display: inline-flex;
    width: 100%;
    justify-content: space-around;
  }
  .container {
    max-width: 600px;
    margin: 0 auto;
    padding: 15px 30px;
    background: #f9f7f5;
  }
</style>
