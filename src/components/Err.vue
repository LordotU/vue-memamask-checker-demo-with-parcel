<template>
  <div id="err" style="color: red;">
    {{ error.message }}
  </div>
</template>

<script>
  export default {
    props: {
      error: Error,
    },
  }
</script>
