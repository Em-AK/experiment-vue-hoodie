<template>
  <div class="hello">
    <h1>Hi {{ user }}!</h1>
    <button @click="signInMyself">Sign In</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return { user: 'World' }
  },
  methods: {
    signInMyself: function () {
      hoodie.account.signIn('emak', 'hohoho')
      this.user = hoodie.account.username
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: #42b983;
}
</style>
