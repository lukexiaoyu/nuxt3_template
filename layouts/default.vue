<script setup>
    import {reactive} from 'vue'
    const datas=reactive({
        adds:[
            {name:'home',link:'/'},
            {name:'one',link:'/one'},
            {name:'css',link:'/css'},
        ]
    })
</script>

<template>
    <div>
      
        <nav>
            <a v-for="x in datas.adds" :href="x.link">{{x.name}}</a>
        </nav>
      <slot />
    </div>
  </template>

<style scoped>
    a{
        margin: 0 5px;
    }
</style>