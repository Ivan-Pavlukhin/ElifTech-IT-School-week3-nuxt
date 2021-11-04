<template>
<div>
    <h1 class="title">{{$route.params.id}}</h1>
    <img class="img__project" :src="projects[$route.params.id]" alt="">
</div>
</template>

<style scoped>
  .title{
    text-align: center;
    margin-top: 20px;
  }
  .img__project{
    display: block;
    width: 480px;
    margin: 20px auto;
  }
</style>

<script>
  import Vue from "vuetify"
  import Component from 'vue-class-component'

  @Component
  export default class Project extends Vue {
    props = {url: String, project: String}

    projects = {
      Project_1: "https://miro.medium.com/max/1838/1*5FF-WiNYehgcBgtgAka1Og.png",
      Project_2: "https://umi.ru/images/cms/data/blog/2105_ux.jpg", 
      Project_3: "https://upload.wikimedia.org/wikipedia/commons/thumb/2/20/NASA_Website_Homepage_-_April_25%2C_2015.png/240px-NASA_Website_Homepage_-_April_25%2C_2015.png", 
      Project_4: "https://www.f-cdn.com/assets/main/en/assets/home/crowd-favorite-redesign/website-1.jpg"
    }
  }
</script>