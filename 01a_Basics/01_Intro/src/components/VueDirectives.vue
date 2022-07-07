<template>
  <!--
      Vue Directives: (v-text, v-once, v-html, v-bind, v-if, v-show)
  -->

  <div>
    <h1 v-if="false" v-text="text">Loading...</h1>
    <h2 v-else-if="false" v-html="link.html" />
    <a
      v-else
      :href="link.url"
      :target="link.target"
      :tabindex="link.tabindex"
      v-text="link.title"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      // v-text
      text: 'Let us know your favorite car and why it is your favorite car and win 2 tickets!',
      // v-bind
      link: {
        url: 'https://www.gims.swiss/',
        target: '_blank',
        tabindex: '0',
        title: 'Find out whats going on!',
        // v-html
        html: '“I am not designed to come second or third. </br> I am designed to win.”<br/><b>- Ayrton Senna</b>',
      },
    }
  },
}
</script>

<style lang="scss" scoped>
h1 {
  color: #242424;
}

h2 {
  margin: 4rem 0 0;
  font-weight: normal;
  color: #e84c47;
}

a {
  display: block;
  margin-top: 4rem;
}
</style>
