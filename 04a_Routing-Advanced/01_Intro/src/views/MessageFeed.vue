<template>
  <div>
    <h1>Feed</h1>
    <div v-for="(m, i) in messages" :key="i" >
      <router-link :to="{ name: 'singlemessage', params: {content: m}}">
        {{ m }}
      </router-link>
    </div>
</div>
</template>
<script>
export default {
  data() {
    return {
      messages: [
        'ALFA ROMEO TONALE: HITTING THE RIGHT NOTES',
        '59th AWARD CEREMONY \'THE CAR OF THE YEAR\' 2022',
        'THE COMBUSTION ENGINE WILL REMAIN IN POLE POSITION FOR SOME TIME YET',
        'WHAT COLOR IS YOUR BUGATTI?'
      ]
    }
  }
}
</script>
