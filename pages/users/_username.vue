<template>
  <h1>
    <h1>user page</h1>
  </h1>
</template>


<script>
  export default {
  validate ({ params }) {
    console.log(params)
    // Must be a name
    return test(params.username)
  }
}
</script>