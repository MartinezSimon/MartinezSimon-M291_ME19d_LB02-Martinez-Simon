<template>
  <div>
    <h1>Single message</h1>
    {{$route.params.content}}
  </div>
</template>

<script>
export default {
  name: "SingleMessage"
}
</script>
