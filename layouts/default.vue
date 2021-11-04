<template>
  <div>
    <v-app-bar elevation="8">
      <span>Header</span>
      <ul class="flex">
        <li class="margin" v-for="(value, key) in menu" :key="key">
          <v-btn elevation="2" :to="value">{{ key }}</v-btn>
        </li>
      </ul>
    </v-app-bar>
    <nuxt />
  </div>
</template>

<style>
  ul{
    list-style: none;
  }
  
  .flex{
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .margin{
    margin: 0 10px;
  }
</style>

<script>
  import Vue from "vuetify"
  import Component from 'vue-class-component'

  @Component
  export default class Header extends Vue {
    menu = {
      home: "/", team: "/ourTeam", about: "/about", gallery: "/gallery"
    }
  }
</script>
