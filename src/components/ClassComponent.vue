<template>
<div class="row">

  <!-- PROFILE USER LEFT -->
  <div id="profile" class="col-2 bg-grey-9">

    <div id="logo" class="row justify-center q-my-sm">
      <span class="logo-my">My</span>
      <span class="logo-jiminy">Jiminy</span>
    </div>

    <div id="userpic" class="column items-center bg-grey-10 q-py-lg">
      <q-avatar size="100px">
      <img src="https://placethedude.com/100/100" alt="">
      </q-avatar>
      <span class="username text-overline">Lebowski</span>
    </div>

    <div class="menu-profile">
      <div class="link-profile row items-center q-my-md q-py-sm">
        <q-icon name="explore" style="font-size:2.5rem" class="col-4"/>
        <span class="col-4" style="text-align: center">Discover</span>
      </div>

      <div class="link-profile row items-center q-my-md q-py-sm">
        <q-icon name="emoji_food_beverage" style="font-size:2.5rem" class="col-4"/>
        <span class="col-4" style="text-align: center">Projects</span>
        <div class="col-4 justify-center items-center" >
        <q-chip size="xs" color="purple-5" text-color="white">14</q-chip>
        </div>
      </div>

      <div class="link-profile row items-center q-my-md q-py-sm">
        <q-icon name="group" style="font-size:2.5rem" class="col-4"/>
        <span class="col-4" style="text-align: center">Contacts</span>
      </div>
    </div>

  </div>

  <!-- CONTENT RIGHT -->
  <div class="col-10 bg-grey-2">

    <div class="hero-img column justify-evenly">
      <div id="pic" class="column items-center">
        <q-avatar size="150px">
        <img src="https://placethedude.com/150/150" alt="">
        </q-avatar>
        <span class="username text-weight-bold text-white text-h5">The Dude</span>
        <span class="text-weight-light text-white text-h6">Producer</span>
      </div>
      <div class="column items-center">
        <q-btn icon="play_arrow" outline rounded color="white" label="Watch his showreel" />
      </div>
    </div>

    <div class="container-content">
    <div class="about">
      <h5>ABOUT ME</h5>
      <p class="text-left">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis tempora consequatur reiciendis, laborum laudantium optio rerum cumque sapiente earum deleniti perferendis doloribus dolore amet, quam nemo accusantium harum consequuntur corporis porro! Ut quod ex ullam rem asperiores dolor aut ad quo laudantium harum! Sapiente vitae ex esse molestiae perferendis beatae suscipit quod eius a laudantium deleniti, quaerat asperiores, alias reprehenderit iste repudiandae ad expedita ut? Reprehenderit, fugiat tempore pariatur debitis distinctio, repellat, velit sed quo mollitia obcaecati iure expedita autem nobis nostrum adipisci omnis eveniet aperiam labore voluptates! Enim quia nesciunt eum quam. Tempore, necessitatibus voluptas ex numquam, molestias quia maiores voluptates modi magnam hic odio cupiditate sint. Quae nobis veniam iure quidem sequi doloribus culpa cumque nesciunt velit autem provident non architecto animi odit, exercitationem eveniet sunt quod rem enim quasi voluptatem ipsam. Consequuntur veritatis praesentium quod ut quasi modi corporis. Blanditiis, eius sint vel beatae, repellat adipisci odit quidem nemo nobis, optio facere voluptas ab ea quisquam reprehenderit aspernatur. Itaque repellat voluptates officia rerum minima quia sequi voluptate illum numquam blanditiis quos dicta corporis aliquid, dolores velit, perferendis quidem dolorum! Et quam minima consectetur laboriosam magnam sequi consequatur temporibus, atque itaque sapiente officia dicta cupiditate, quisquam excepturi labore!</p>
    </div>

      <!-- PROJECTS GRID -->
    <div class="projects column justify-center">
      <h5 class="text-center">SOME OF MY WORK</h5>

      <div class="row row-grid">
        <div class="column column-grid">
          <img src="https://placethedude.com/300/250" alt="">
          <img src="https://placethedude.com/250/250" alt="">
        </div>

        <div class="column column-grid">
          <img src="https://placethedude.com/500/250" alt="">
          <img src="https://placethedude.com/600/300" alt="">
          <img src="https://placethedude.com/400/250" alt="">
        </div>

        <div class="column column-grid">
          <img src="https://placethedude.com/300/250" alt="">
          <img src="https://placethedude.com/400/450" alt="">
        </div>
      </div>

      <div class="row flex-center">
        <q-btn color="purple-5" label="Watch portfolio" padding="sm 150px"/>
      </div>

    </div>

    <div class="talk-about">
        <h5 class="text-center q-mt-xl q-mb-none">THEY TALK ABOUT ME...</h5>
        <q-carousel
        v-model="slide"
        transition-prev="scale"
        transition-next="scale"
        swipeable
        animated
        control-color="grey"
        navigation
        padding
        arrows
        height="300px"
        class="bg-white text-grey rounded-borders"
      >
        <q-carousel-slide name="style" class="row no-wrap flex-center">
          <div class="col-2 text-center">
          <q-avatar size="100px">
          <img src="https://placethedude.com/100/100" alt="">
          </q-avatar>
          </div>
          <div class="col-4">
          <div class="row">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sint quisquam neque molestiae repellat, accusamus et officia consequatur! Molestias debitis necessitatibus consequatur suscipit vitae temporibus optio.
          </div>
          <span class="row text-weight-bold justify-end">"Jordan Little"</span>
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="style"></q-carousel-slide>
        <q-carousel-slide name="style"></q-carousel-slide>
        <q-carousel-slide name="style"></q-carousel-slide>
        </q-carousel>

    </div>
  </div>

</div>

    <!-- <p>Count: {{ todoCount }} / {{ meta.totalCount }}</p>
    <p>Active: {{ active ? 'yes' : 'no' }}</p>
    <p>Clicks on todos: {{ clickCount }}</p> -->
</div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator'
import { Todo, Meta } from './models'

@Component
export default class ClassComponent extends Vue {
  @Prop({ type: String, required: true }) readonly title!: string;
  @Prop({ type: Array, default: () => [] }) readonly todos!: Todo[];
  @Prop({ type: Object, required: true }) readonly meta!: Meta;
  @Prop(Boolean) readonly active!: boolean;

  titre = 'hello';

  clickCount = 0;

  increment () {
    this.clickCount += 1
  }

  get todoCount () {
    return this.todos.length
  }

  data () {
    return {
      slide: 'style',
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
  }
}
</script>

<style scoped>

/*PROFILE*/

#profile{
  color: white;
}
#logo{
  font-size: 2rem;
}
.logo-my{
  color: rgb(188, 72, 235);
}
.logo-jiminy{
  font-weight: bold;
}

.link-profile:hover{
  background-color:rgb(188, 72, 235) ;
  color: rgb(58, 58, 58);
}

/* HERO */

.hero-img{
  background-repeat: no-repeat;
  height: 100vh;
  background-size: cover;
  background-image: url("https://hdqwalls.com/wallpapers/best-nature-image.jpg");
}

/* CONTAINER CONTENT */

.container-content{
  max-width: 90%;
  margin: 0 auto;
}

/* ABOUT */

.about{
  margin: 0 auto;
  margin-top: 3rem;
  margin-bottom: 3rem;
  text-align: center;
  border: 1px darkgrey solid;
  background: white;
  padding: 0 5rem;
  padding-bottom: 2rem;
}

/* PROJECTS GRID */

.row-grid {
  display: flex;
  flex-wrap: wrap;
}

.column-grid {
  flex: 33%;
  max-width: 33%;
  padding: 0 4px;
  padding-bottom: 7rem;
}

.column-grid img {
  margin-top: 8px;
  vertical-align: middle;
  width: 100%;
}

/* TALK ABOUT */

.talk-about{
  margin: 0 auto;
  margin-top: 3rem;
  margin-bottom: 3rem;
  border: 1px darkgrey solid;
  background: white;
  padding: 0 2rem;
  padding-bottom: 2rem;
}
</style>
