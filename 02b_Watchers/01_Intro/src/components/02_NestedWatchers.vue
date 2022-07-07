<template>
  <div class="container">
    <h1>Carshow Tickets</h1>
    <div>
      <h2>{{ product.label }}</h2>
      <h5>CHF {{ product.price }} (Fr. {{ discount }} cheaper)</h5>
      <a href="#" @click="updatePrice">Reduce price</a>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      discount: 0,
      product: {
        price: 60,
        label: 'Carshow Genf 2022',
      },
    }
  },
  methods: {
    updatePrice(){
      if (this.product.price < 1) return;
      this.product.price--;
    }
  },
  watch: {
    'product.price'(newVal,oldVal){
      this.discount++;
      console.log(`actual(CHF ${newVal}) and old(CHF ${oldVal}) price.`);
    }
  }
}
</script>
<style lang="scss" scoped>
.container {
  margin: 0 auto;
  padding: 30px;
  max-width: 600px;
  font-family: 'Verdana', Helvetica, sans-serif;
  margin: 0;
}
a {
  display: inline-block;
  background: #083d70;
  border-radius: 10px;
  font-size: 14px;
  color: white;
  padding: 10px 20px;
  text-decoration: none;
}

h1 {
  color: #242424;
}

h2 {
  font-weight: normal;
  color: #e84c47;
}
</style>
