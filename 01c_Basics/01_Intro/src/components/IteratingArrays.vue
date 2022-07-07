<template>
  <div>
    <h1>Which car brands made it to last years podium?</h1>
    <h2>The best three constructors and our 2021 championship winner.</h2>
    <ul>
      <li id="li-title" v-for="item in interests" :key="item">
        {{ item.title }}
        <ol>
          <li id="li-content" v-for="fav in item.favorite" :key="fav"> {{ fav }}</li>
        </ol>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      interests: [
        {title:"Mercedes", favorite:["Amg Project One", "W13 - F1 Contructor Championship Winner 2014 -2021 ", "EQS - Electric Car"]},
        {title:"Ferrari", favorite:["Purosange - Ferraris first SUV", "Ferrari SF90 - hybrid", "Ferrari F1-75"]},
        {title:"BMW", favorite:["M3 Touring", "M4 GT3", "M4 - Redbull Drift Brothers edition"]}
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
#li-title {
  font-family: 'Verdana', Helvetica, Arial, sans-serif;
  color: #494949;
  margin-top: 1.5rem;
  font-weight: bold;
}

#li-content {
  font-family: 'Verdana', Helvetica, Arial, sans-serif;
  color: #382f2f;
  font-weight: normal;
}

h1 {
  font-family: 'Verdana', Helvetica, Arial, sans-serif;
  color: #242424;
  margin-top: 60px;
}

h2 {
  font-family: 'Verdana', Helvetica, Arial, sans-serif;
  color: #e84c47;
}
</style>
