<template>
  <div class="hello">
    <b-button class="m-5" size="lg" variant="outline-dark" @click="logout">Logout</b-button>
  </div>
</template>

<script>
import firebase from 'firebase';
export default {
  name: 'HelloWorld',
  methods: {
    logout() {
      firebase.auth().signOut().then(() => {
        this.$router.replace('/login');
      }).catch((error) => {
        console.log(error);
      });
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
