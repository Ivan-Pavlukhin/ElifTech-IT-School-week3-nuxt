<template>
<div>
    <h1 class="title">About</h1>
    <ul class="flex">
        <li class="article" v-for="article of articles" :key="article.title">
            <h2 class="title">{{article.title}}</h2>
            <p class="text">{{article.article}}</p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Maiores laboriosam aliquam saepe sequi mollitia. Fuga aliquid est itaque voluptates architecto aut pariatur. Magni facilis suscipit dignissimos minus quia pariatur mollitia sed tenetur cumque officiis reiciendis dolorem quo consectetur nihil animi nesciunt cupiditate earum expedita numquam possimus, labore quidem id provident! Expedita laboriosam deserunt, ut nihil magni voluptatibus culpa quis in fuga, nisi natus inventore odio obcaecati cumque voluptatem facere, repellat laudantium? Dolores vel pariatur et nemo laborum praesentium, ratione voluptas necessitatibus. Corporis, alias pariatur. Maxime, voluptates laborum asperiores accusantium magni nulla quas, minima aperiam facere et, consectetur laudantium unde distinctio!
        </li>
    </ul>
</div>
</template>

<style scoped>
    .title{
        text-align: center;
        margin-top: 20px;
    }
    .article{
        width: calc(100% / 2 - 40px);
        margin: 20px;
    }
    .text{
        margin-top: 15px;
    }
</style>

<script>
  import Vue from "vuetify"
  import Component from 'vue-class-component'

  @Component
  export default class Person extends Vue { 
      articles = [
          {title: "About us",
          article: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Maiores laboriosam aliquam saepe sequi mollitia. Fuga aliquid est itaque voluptates architecto aut pariatur. Magni facilis suscipit dignissimos minus quia pariatur mollitia sed tenetur cumque officiis reiciendis dolorem quo consectetur nihil animi nesciunt cupiditate earum expedita numquam possimus, labore quidem id provident! Expedita laboriosam deserunt, ut nihil magni voluptatibus culpa quis in fuga, nisi natus inventore odio obcaecati cumque voluptatem facere, repellat laudantium? Dolores vel pariatur et nemo laborum praesentium, ratione voluptas necessitatibus. Corporis, alias pariatur. Maxime, voluptates laborum asperiores accusantium magni nulla quas, minima aperiam facere et, consectetur laudantium unde distinctio!"
          },
          {title: "responsibilities",
          article: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Maiores laboriosam aliquam saepe sequi mollitia. Fuga aliquid est itaque voluptates architecto aut pariatur. Magni facilis suscipit dignissimos minus quia pariatur mollitia sed tenetur cumque officiis reiciendis dolorem quo consectetur nihil animi nesciunt cupiditate earum expedita numquam possimus, labore quidem id provident! Expedita laboriosam deserunt, ut nihil magni voluptatibus culpa quis in fuga, nisi natus inventore odio obcaecati cumque voluptatem facere, repellat laudantium? Dolores vel pariatur et nemo laborum praesentium, ratione voluptas necessitatibus. Corporis, alias pariatur. Maxime, voluptates laborum asperiores accusantium magni nulla quas, minima aperiam facere et, consectetur laudantium unde distinctio!"}
      ]
  }
</script>