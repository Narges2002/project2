<template>
    <div id="app">
        <link rel="stylesheet" type="text/css" href="./assets/css/all.min.css">
        <Header/>
        <Section/>
        <Section1/>
        <Section2/>
        <Section3/>
        <Section4/>
        <Section5/>
        <Section6/>
        <Section7/>
        <Test/>
        <Footer/>
    </div>
</template>

<script>
import Header   from  './components/Header.vue'
import Section  from  './components/Section.vue'
import Section1 from  './components/Section1.vue'
import Section2 from  './components/Section2.vue'
import Section3 from  './components/Section3.vue'
import Section4 from  './components/Section4.vue'
import Section5 from  './components/Section5.vue'
import Section6 from  './components/Section6.vue'
import Section7 from  './components/Section7.vue'
import Footer   from  './components/Footer.vue'
import Test   from  './components/Test.vue'

export default {
  name: 'App',
  components: {
    Header,
    Section,
    Section1,
    Section2,
    Section3,
    Section4,
    Section5,
    Section6,
    Section7,
    Footer,
    Test
  }
}
</script>

<style>
  @import './assets/css/style.css';
#app {
  font-family: IRANSansWeb;
  direction: rtl;
}
</style>