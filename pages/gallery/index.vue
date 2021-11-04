<template>
    <div>
        <h1 class="title">Gallery</h1>
        <ul class="flex projects">
            <li class="card" v-for="(value, key) in projects" :key="key">
                <NuxtLink class="link" :to="`/gallery/${key}`"><h2 class="title">{{ key }}</h2> <img :src="value" alt=""></NuxtLink>
            </li>
        </ul>
    </div>
</template>
<style scoped>
  img{
   width: 100%;
   height: auto; 
  }
  .title{
    text-align: center;
  }
  .flex{
    display: flex;
    align-items: stretch;
  }
  .card{
    width: calc(100% / 4 - 40px);
    margin: 20px;
  }
  .link{
    text-decoration: none;
    color: black;
  }
</style>
<script>
  import Vue from "vuetify"
  import Component from 'vue-class-component'

  @Component
  export default class Gallery extends Vue {
    projects = {
      Project_1: "https://miro.medium.com/max/1838/1*5FF-WiNYehgcBgtgAka1Og.png",
      Project_2: "https://umi.ru/images/cms/data/blog/2105_ux.jpg", 
      Project_3: "https://upload.wikimedia.org/wikipedia/commons/thumb/2/20/NASA_Website_Homepage_-_April_25%2C_2015.png/240px-NASA_Website_Homepage_-_April_25%2C_2015.png", 
      Project_4: "https://www.f-cdn.com/assets/main/en/assets/home/crowd-favorite-redesign/website-1.jpg"
    }
  }
</script>