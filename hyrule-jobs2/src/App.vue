<template>
  <div class="app">
    <!-- hello, hyrule
    <p>{{ name }}</p>
    <p>{{age}}</p>
    <button @click="changeName('Zelda')">change name</button>
    <button @click="changeAge(23)">change age </button> -->
    <p> {{jobs[0].location}}</p>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs, ref  } from 'vue';

import HelloWorld from './components/HelloWorld.vue';

import Job from './types/Job';

export default defineComponent({
  name: 'App',
 

  setup(){

    const jobs =  ref<Job[]>([
      {title: 'farm worker' , location : 'lon lon ranch', salary:300000, id:1},
      {title:'quarryman', location:'death mountain', salary:40000, id:2},
      {title:'flute player' , location:'the lost woods ' , salary:40000, id:3},
      {title:'fisherman' , location:'lake hylia' , salary:300000 , id:3},

    ])

    return {jobs}
    // const state = reactive({  
    //   nanme:'Link',
    //   age:25 as string | number 
    // })

    // return {  ...toRefs(state)}

    // const name = ref('Link')
    // const age = ref<number | string>(25)
  },

  // data() { 
  //   return { 
  //     name:'Link',
  //     age:25 as number | string 
  //   } 
  // },

  // methods: { 
  //   changeName(name:string) 
  //    { 
  //     this.name = name; 
  //     return name
  //    },
  //    changeAge(age:number)
  //    {
  //     this.age = age;
  //     return age
  //    }
  // }

});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
