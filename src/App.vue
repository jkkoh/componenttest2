<script setup>
import{ ref } from 'vue'
import BlogPost from './components/BlogPost.vue'
import SecondPost from './components/SecondPost.vue'

const posts = ref([
  { id: 1, title: 'Vue 12345' },
  { id: 2, title: 'Vue aaaaaa' } ,
  { id: 3, title: 'Vue cccccccc' }  
])

const phobs = ref([
  { id: 1, second: 'Vue eeeee' },
  { id: 2, second: 'Vue fffff' } ,
  { id: 3, second: 'Vue ggggg' }  
])
</script>

<template>
  <h2>first post</h2> <!--yes script setup-->
  <BlogPost 
    v-for="post in posts" 
    :key="post.id" 
    :title="post.title"
  ></BlogPost>
<br/>
<h2>second post</h2> <!--no script setup-->
  <SecondPost
    v-for="phob in phobs" 
    :key="phob.id" 
    :second="phob.second"
  ></SecondPost>
</template>

