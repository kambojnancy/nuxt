<template>
  <h1>
    <h1>id page</h1>
  </h1>
</template>


<script>
  export default {
  validate ({ params }) {
    console.log(params)
    // Must be a number
    return /^\d+$/.test(params.id)
  }
}
</script>