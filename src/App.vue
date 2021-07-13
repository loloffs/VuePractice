<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <Navbar 
    mainHeading="Vue Practice"
    subHeading="A job application form for practice purposes"
    logo="https://neufert-cdn.archdaily.net/uploads/account_logo/logo/1795/large_large_article_logo_400x125__1_.png"
  />
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <div id="applicationContainer">
    <Form
      companyName="Article"
      positionTitle="Junior Developer"
      citizenship="Canadian"
    />
    <HiringInfo 
      img="https://i.pinimg.com/originals/51/f6/fb/51f6fb256629fc755b8870c801092942.png"
      name="John Smith"
      title="Engineering Manager"
      email="examle@email.com"
      phone="123-456-7890"
    />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Form from './components/Form.vue'
import HiringInfo from './components/HiringInfo.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Form,
    HiringInfo
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#applicationContainer{
  display: flex;
}
</style>
