<template>
     <section class="split-section" id="Contact">
        <div class="left">
            <div class="left-content">
                <h2>Nous rendre visite</h2>
                <p>Ivoire Trade Center, Cocody, Abidjan, Côte d'Ivoire</p>

                <h2>Heures d'ouverture</h2>
                <p>Lun - Jeu: 10h - 23h</p>
                <p>Ven - Dim: 13h - 23h</p>
            </div>
        </div>
        <div class="right">
            <div class="right-content">
                <h2>Nous Contactez</h2>
                <p>Email: xyz@yahoo.fr</p>
                <p>Appel: 2724303890</p>
            </div>
        </div>
    </section>
<!--     <a href="#" class="back-to-top-btn" @click="scrollToTop">
      <i class="fa-solid fa-arrow-up"></i>
    </a> -->
</template>

<script>

export default{
    name: 'Contact',
    methods: {
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: "smooth" });
    },
  },
}
</script>

<style>

@import '../style.css';
</style>