<template>
  <div class="hiringInfo">
    <img id="avatar" :src="`${img}`" />
    <h3>{{ name }}</h3>
    <h5>{{ title }}</h5>
    <a href="mailto:example@email.com">{{ email }}</a>
    <h6>{{ phone }}</h6>
  </div>
</template>

<script>
export default {
  name: 'HiringInfo',
  props: {
    img: Image,
    name: String,
    title: String,
    phone: String,
    email: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hiringInfo {
  display: flex;
  align-items: center;
  justify-content: end;
  flex-direction: column;
  width: 100%;
  margin-right: 2em;
  margin-top: 5em;
}
h1 {
  margin: 10px 0 0 0;
}
h3 {
  margin: 10px 0 0 0;
}
h5 {
  margin: 10px 0 0 0;
}
h6 {
  margin: 10px 0 0 0;
}
#avatar {
  width: 10em;
  height: auto;
}
</style>
