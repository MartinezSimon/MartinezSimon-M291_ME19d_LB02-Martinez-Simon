<template>
  <div>
    <h1>Cart</h1>
    <table>
      <thead>
      <tr>
        <th>Name</th>
        <td>&nbsp;&nbsp;&nbsp;</td>
        <th>Amount</th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="(product, idx) in cart" :key="idx">
        <td>{{ product.name }}</td>
        <td>{{ product.quantity  }}</td>
      </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import { mapState } from 'vuex';
export default {
  name: 'Cart',
  computed: mapState(['cart'])
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
</style>
