<template>
  <div>
    <go-back></go-back>
    <h1>
      Hello!
      <small class="text-muted">I am page 2!</small>
    </h1>
    <p>An example of using this.$router.push()</p>
    <button @click="goToHome" class="btn">Go Home</button>
    <hr />
    <router-view></router-view>
  </div>
</template>
 
 <style scoped>
.text-muted {
  color: gray;
  font-weight: lighter;
}
</style>

<script>
import GoBack from "../components/GoBackButton";

export default {
  components: {
    "go-back": GoBack
  },
  methods: {
    goToHome: function() {
      // console.log(this.$router);

      // this.$route and this.$router are different!!!
      this.$router.push({ path: "/" });
    }
  }
};
</script>