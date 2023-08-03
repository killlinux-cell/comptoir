<template>
  <Navbar></Navbar>
  <Hero></Hero>
  <Menu></Menu>
  <Contact></Contact>
  <Footer></Footer>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import Menu from './components/Menu.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';


export default {
	name: "App",
	components: {
    Navbar,
    Hero,
    Menu,
    Contact,
    Footer,
	},
};
</script>

<style scoped>
@import "./style.css";
</style>
