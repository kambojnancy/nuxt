<template>
  <div>
    <h5 v-if="loading">Loading....</h5>
    <article v-for="post in posts">
      <h1>{{ post.title }}</h1>
      <p>{{ post.body }}</p>
    </article>
  </div>
</template>

<script>
  import axios from 'axios'

  export default {
    layout: 'blog',

     data() {
        return {
          loading: true,
          posts: []
        }
     },
     mounted() {
      this.getPosts();
     },
     methods: {
      async getPosts() { 
         let vm = this       
         let { data } = await axios.get(`https://jsonplaceholder.typicode.com/posts`)
         vm.posts = data
         vm.loading = false
      }
     }
  }
</script>