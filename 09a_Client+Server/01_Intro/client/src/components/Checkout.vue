<template>
  <div>
    <h1>Checkout</h1>
    Total amount {{ cartTotal.toFixed(2) }}.<br>
    <b-button variant="primary" v-show="cartTotal > 0" @click="checkout">Checkout</b-button>
  </div>
</template>

<script>
import {mapGetters} from 'vuex';

export default {
  name: 'Cart',
  computed: mapGetters(['cartTotal']),
  methods: {
    checkout() {
      alert('Checkout processed!');
    }
  }
}
</script>

<style lang="scss" scoped>
body {
  font-family: 'Verdana', Helvetica, Arial, sans-serif;
  margin: 10%;
  background-color: #e8e8e8;
}
h1 {
  color: #242424;
}

h2 {
  font-weight: normal;
  color: #e84c47;
}

th {
  font-weight: bold;
  color: #3f5462;
}

button{
  background-color: #083d70;
  border-color: #083d70;
}
</style>