<template>
  <div>
    <h1 class="title">{{$route.params.id}}</h1>
    <img class="img" :src="team[$route.params.id]" alt="">
  </div>
</template>
<style scoped>
  .img{
    display: block;
    margin: 20px auto;
    max-width: 480px;
  }
  .title{
    text-align: center;
    margin-top: 20px;
  }
</style>
<script>
  import Vue from "vuetify"
  import Component from 'vue-class-component'

  @Component
  export default class Person extends Vue { 
    team = {
      Ivan: 'https://img.freepik.com/free-photo/waist-up-portrait-of-handsome-serious-unshaven-male-keeps-hands-together-dressed-in-dark-blue-shirt-has-talk-with-interlocutor-stands-against-white-wall-self-confident-man-freelancer_273609-16320.jpg?size=626&ext=jpg',
      Yan: 'https://img.freepik.com/free-photo/young-handsome-man-with-beard-over-isolated-keeping-the-arms-crossed-in-frontal-position_1368-132662.jpg?size=626&ext=jpg',
      Olga: 'https://img.freepik.com/free-photo/young-and-beautiful-woman-in-pink-warm-sweater-natural-look-smiling-portrait-on-isolated-long-hair_285396-896.jpg?size=626&ext=jpg',
      Vova: 'https://images.unsplash.com/photo-1568602471122-7832951cc4c5?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8bWFufGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&w=1000&q=80',
      
    } 
      }
    
</script>