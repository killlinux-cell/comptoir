<template>
     <section class="split-section" id="Contact">
        <div class="left">
            <div class="left-content">
                <h2>Nous rendre visite</h2>
                <br>
                <p>Ivoire Trade Center, Cocody, Abidjan, Côte d'Ivoire</p>
                <br>

                <h2>Heures d'ouverture</h2>
                <br>
                <p>Lun - Jeu: 10h - 23h</p>
                <br>
                <p>Ven - Dim: 13h - 23h</p>
            </div>
        </div>
        <div class="right">
            <div class="right-content">
                <h2>Nous Contactez</h2>
                <br>
                <p>Email: xyz@yahoo.fr</p>
                <br>
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