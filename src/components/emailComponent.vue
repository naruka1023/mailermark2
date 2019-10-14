<template>
  <div style='padding:20px'>{{email}}</div>  
</template>

<script>
  import routes from '../routes'

  export default {
    props: {
      email: {
        type:String,
        required: true 
      }
    },
    computed: {
      isActive () {
        return this.href === this.$root.currentRoute
      }
    },
    methods: {

    }
  }
</script>

<style scoped>
  .active {
    color: cornflowerblue;
  }
</style>
