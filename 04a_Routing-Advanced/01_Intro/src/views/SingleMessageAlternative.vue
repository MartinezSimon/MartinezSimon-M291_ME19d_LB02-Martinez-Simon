<template>
  <div>
    <h1>Single message</h1>
       {{content}}
  </div>
</template>

<script>
export default {
  name: "SingleMessage",
  props: {
    content: {
      default: '',
      type: String
    }
  }
}
</script>
