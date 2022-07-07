<!--demo-01a: Implementing and Adding a Message Feed Page Using Vue Router -->
<template>
  <div>
    <h1>Message from GIMS</h1>
    <p v-for="(m, i) in messages" :key="i">
      {{ m }}
    </p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      messages: [
        'SAVE THE DATE',
        'We are very happy to confirm you that the Geneva International Motor Show will be on\n' +
        'from February 14th to February 19th 2023 in Palexpo, Geneva.',
        'CONTACT',
        'Geneva International Motor Show, \n' +
        'Route François-Peyrot 30, \n' +
        '1218 Le Grand-Saconnex - Suisse'
      ]
    }
  }
}
</script>
