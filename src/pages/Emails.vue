<template>
  <main-layout>
    <p>List of Emails</p>
    <div v-if=flag>
      
      <email-component
        v-for = "(item, index) in emailList"
        v-bind:key = 'index'
        v-bind:email = 'item'>
      </email-component>
    </div>
    <div style='margin-bottom:20px' v-else>List is empty!</div>
    <button @click='addEmail'>Add New Emails</button>
    
  </main-layout>
</template>

<script>
  import MainLayout from '../layouts/Main.vue'
  import emailComponent from '../components/emailComponent.vue'

  export default {
    data: () => {
      return {
        emailList:[],
        flag : false
      }
    },
    watch:{
      emailList:function(){
        (this.emailList.length == 0)? this.flag = false : this.flag = true; 
      }
    },
    methods:{
      addEmail: function(){
        this.emailList.push('vbrewbvrtw');
      }
    },
    components: {
      MainLayout,
      emailComponent
    }
  }
</script>
