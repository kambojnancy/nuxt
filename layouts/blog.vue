<template>
  <div>
  <Header/>
    <h1>List of blog posts</h1>
    
    <nuxt/>
  </div>
</template>

<script>
  import Header from '~/components/Header'

  export default {
    components: {
      Header
    }
  }
</script>