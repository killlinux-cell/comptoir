<template>
<nav class="nav-conatiner">
        <div class="logo">
            <!-- Mettez votre logo ici -->
            <a href="#accueil"> Le Comptoir</a>
        </div>
        <div class="nav-middle">
            <ul class="nav-links">
                <li><a href="#hero-section">ACCUEIL</a></li>
                <li><a href="#Contact">A PROPOS</a></li>
                <!-- <li><a href="#menu">MENU</a></li> -->
                <div class="menu-dropdown">
					<a
						href="#menu-section"
						class="dropbtn nav"
						@mouseenter="showDropdown"
						@mouseleave="hideDropdown"
						>MENU</a
					>
					<div
						class="dropdown-content"
						@mouseenter="showDropdown"
						@mouseleave="hideDropdown"
						v-show="isDropdownVisible"
					>
						<a @click="triggerModal" href="#menu-section">Avis du chef</a>
					</div>
				</div>
                <li><a href="#Contact">CONTACT</a></li>
            </ul>
        </div>
        <div class="nav-right">
         <a href="" class=" btn-nav">FIND A TABLE</a>
        </div>
        <!-- hambuger menu -->
        <div class="hamburger-menu-container" @click="openMenu">
				<div
					class="hamburger-menu"
					:class="{ close: isActive }"
					id="toggle-menu"
				></div>
			</div>
        <!-- hambuger menu -->
        <!-- responsive mobile -->
        <div class="nav-mobile">
			<a href="#hero-section" class="mobile-element" @click="openMenu">Accueil</a>
			<a href="#Contact" class="mobile-element" @click="openMenu">A propos</a>
			<a href="#menu" class="mobile-element" @click="openMenu">Menu</a> 
			<a href="#Contact" class="mobile-element" @click="openMenu">Contact</a>
		</div>
        <!-- responsive mobile -->
    </nav>
</template>

<script>
export default {
	name: "Navbar",
    data() {
		return {
			isScrolled: false,
			isActive: false,
			isDropdownVisible: false,
		};
	},
	created() {
		window.addEventListener("scroll", this.onScroll);
	},
	destroyed() {
		window.removeEventListener("scroll", this.onScroll);
	},
	methods: {
		onScroll(event) {
			this.isScrolled = window.scrollY > 0;
		},

		openMenu(event) {
			const toggleButton = document.getElementsByClassName("hamburger-menu")[0];
			const navLinks = document.getElementsByClassName("nav-mobile")[0];

			if (this.isActive == false) {
				navLinks.style.transform = "translate(-100%, 0)";
				this.isActive = true;
			} else if (this.isActive == true) {
				navLinks.style.transform = "translate(100%, 0)";
				this.isActive = false;
			}
		},
		showDropdown() {
			this.isDropdownVisible = true;
		},
		hideDropdown() {
			this.isDropdownVisible = false;
		},
		triggerModal() {
			this.$emit("showModal");
		},
	},
};
</script>

<style scoped>
@import "../style.css";
</style>
