<template>
  <div class="navbar">
    <img id="logo" alt="logo" :src="`${logo}`">
    <h1>{{ mainHeading }}</h1>
    <p>{{ subHeading }}</p>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  props: {
    mainHeading: String,
    subHeading: String,
    logo: Image
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
  background-color: black;
  width: 100%;
  /* position: sticky; */
  top: 0;
  z-index: 10000;
}
h1 {
  margin: 10px 0 0 0;
  color: grey;
}
#logo {
  width: 5em;
  height: auto;
}
p {
  color: grey;
}
</style>
