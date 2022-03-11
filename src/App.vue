<template>
    <div id="app">
        <div class="container">
          <link rel="stylesheet" type="text/css" href="./assets/css/all.min.css">
          <Header/>
          <Section1/>
          <Section2/>
          <Section3/>
          <Section4/>
          <Section5/>
          <Footer/>
        </div>
    </div>
</template>

<script>
import Header   from  './components/Header.vue'
import Section1 from  './components/Section1.vue'
import Section2 from  './components/Section2.vue'
import Section3 from  './components/Section3.vue'
import Section4 from  './components/Section4.vue'
import Section5 from  './components/Section5.vue'
import Footer   from  './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Section1,
    Section2,
    Section3,
    Section4,
    Section5,
    Footer,
  }
}
</script>

<style>
.container {
  max-width: 450px !important;
}
  @import './assets/css/style.css';
#app {
  font-family: IRANSansWeb;
}
</style>