<template>
  <div class="container">
    <div class="user-input">
      <button class="button--navi" @click="goHome()">Home | Start</button>
      <button class="button--navi" @click="goBack()">Previous</button>
      <button class="button--navi" @click="goForward()">Next</button>
    </div>
  </div>
</template>


<script>
export default {
  methods: {
    goHome() {
      this.$router.push('/');
    },
    goBack() {
      this.$router.go(-1);
    }, goForward() {
      this.$router.go(1);
    }
  }
}
</script>

<style lang="scss">

$color-darkgrey: #2c3e50;

.container {
  max-width: 80%;
  margin: 8rem auto;
}


.user-input {
  display: flex;
  align-items: center;
  padding-bottom: 20px;

  input {
    width: 100%;
    padding: 10px 6px;
    margin-right: 10px;
  }
}

h1 {
  color:#242424;
}

h2 {
  font-weight: normal;
  color: #e84c47;
}

// Buttons
button {
  appearance: none;
  padding: 10px;
  margin: 2px;

  font-weight: bold;
  border-radius: 10px;
  border: none;
  background: $color-darkgrey;
  color: white;
  white-space: nowrap;

  + button {
    margin-left: 10px;
  }
}

.button--navi {
  display: block;
  margin: 0 auto;
  background: #083d70;
}

</style>
