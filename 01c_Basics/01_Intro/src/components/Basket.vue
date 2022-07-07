<template>
  <div class="container">
    <h1>Carshow Genf</h1>
    <h2>Shopping Cart: (Article: {{ totalItems }}) {{ formatPrize("Fr.",totalCost) }}</h2>
    <div class="even-columns" v-for="item in products" :key="item">
      <div class="col">{{ item.title }}</div>
      <div class="col"><a href="#" @click="addToCart(item.prize)">Add {{ formatPrize(item.currency, item.prize) }}</a></div>
    </div>

  </div>
</template>

<script>
export default {
  data() {
    return {
      totalItems: 0,
      totalCost: 0,
      products: [
        {title:"Toddler 0-3", currency: "Fr.", prize: 5},
        {title:"Kids 4-12", currency: "Fr.", prize: 20},
        {title:"Teenager 13-17", currency: "Fr.", prize: 40},
        {title:"Adult 18+", currency: "Fr.", prize: 60},
      ],
    }
  },
  methods: {
    addToCart(n) {
      this.totalItems = this.totalItems + 1
      this.totalCost = this.totalCost + n
    },
    formatPrize(currency, val) {
      return `${currency} ${val.toFixed(2)}`
    },
  },
}
</script>

<style lang="scss" scoped>

h1 {
  font-family: 'Verdana', Helvetica, Arial, sans-serif;
  color: #242424;
  margin-top: 10%;
}

h2 {
  font-family: 'Verdana', Helvetica, Arial, sans-serif;
  color: #e84c47;
}

.even-columns {
  display: flex;
  //gap: 0.1em;
  padding: 0.2em;
}

.even-columns > * {
  flex: 1;
}

.card {
  padding: 2em;
  background: var(--clr-gradient);
  color: white;
  border-radius: 0.25rem;
}


*,
*::before,
*::after {
  box-sizing: border-box;
}

:root {
  --clr-primary: #083d70;
  --clr-secondary: #ff0000;
  --clr-accent: #d5d5d5;
  --clr-gradient: linear-gradient(
          -90deg,
          var(--clr-primary),
          var(--clr-secondary)
  );
  --ff-title: bungee, sans-serif;
  --ff-body: canada-type-gibson, sans-serif;
  --fw-body: 300;
  --fw-bold: 800;
  --fw-title: 400;
  --fw-number: 800;
}

body {
  min-height: 80vh;
  font-family: var(--ff-body);
  font-weight: var(--fw-body);
  font-size: 1.25rem;
  display: flex;
  flex-direction: column;
}

a {
  display: inline-block;
  background: #083d70;
  border-radius: 10px;
  font-size: 10px;
  color: white;
  padding: 5px 10px;
  text-decoration: none;
}
.container {
  margin: 0 auto;
}
</style>
