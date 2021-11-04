<template>
    <div>
        <h1 class="title">Our Team</h1>
        <ul class="flex">
            <li class="card"  v-for="person of team" :key="person.name">
                <nuxt-link :to="`/ourTeam/${person.name}`"> <img :src="person.img" alt="" /> <span class="purple darken-3">{{ person.name }}</span></nuxt-link>
            </li>
        </ul>
    </div>
</template>

<style scoped>
  
  .title{
        text-align: center;
        margin-top: 40px;
    }

  a{
    display: block;
    color: inherit;
    font-weight: 700;
    font-size: 20px;
    text-decoration: none;
    text-align: center;
    
  }

  img{
    width: 100%;
    height: auto;
  }

  .card{
    width: calc(100% / 4 - 30px);
    margin: 15px;
  }
</style>

<script>
  import Vue from "vuetify"
  import Component from 'vue-class-component'

  @Component
  export default class Team extends Vue {
    team = [
      {name: "Ivan", 
      img: 'https://img.freepik.com/free-photo/waist-up-portrait-of-handsome-serious-unshaven-male-keeps-hands-together-dressed-in-dark-blue-shirt-has-talk-with-interlocutor-stands-against-white-wall-self-confident-man-freelancer_273609-16320.jpg?size=626&ext=jpg'
      },
      {name: "Yan", 
      img: 'https://img.freepik.com/free-photo/young-handsome-man-with-beard-over-isolated-keeping-the-arms-crossed-in-frontal-position_1368-132662.jpg?size=626&ext=jpg'
      },
      {name: "Olga", 
      img: 'https://img.freepik.com/free-photo/young-and-beautiful-woman-in-pink-warm-sweater-natural-look-smiling-portrait-on-isolated-long-hair_285396-896.jpg?size=626&ext=jpg'
      },
      {name: "Vova", 
      img: 'https://images.unsplash.com/photo-1568602471122-7832951cc4c5?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8bWFufGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&w=1000&q=80'
      }
    ]

    getImgUrl(pet) {
    // var images = require.context('../static/', false, /\.png$/)
    return ('public/' + pet)
  }
  }
</script>