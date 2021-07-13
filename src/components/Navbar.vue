<template>
  <div class="navbar">
    <h1>Thank you for your interest in {{ companyName }}</h1>
    <p>{{subheading}}</p>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  props: {
    companyName: String,
    subheading: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.navbar {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  background-color: grey;
  width: 100%;
  position: sticky;
  top: 0;
}
h1 {
  margin: 10px 0 0 0;
}
</style>
