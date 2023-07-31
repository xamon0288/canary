<template>
	<section id="nav-section">
		<div class="nav-container" :class="{ scrolled: isScrolled }">
			<div class="nav-logo">
				<a href="/"><h2 class="logo">CANARI</h2></a>
			</div>
			<div class="nav-elements" id="nav-links">
				<a href="#hero-section" class="nav">Accueil</a>
				<a href="#about-section" class="nav">A propos</a>

				<div class="menu-dropdown">
					<a
						href="#menu-section"
						class="dropbtn nav"
						@mouseenter="showDropdown"
						@mouseleave="hideDropdown"
						>Menu</a
					>
					<div
						class="dropdown-content"
						@mouseenter="showDropdown"
						@mouseleave="hideDropdown"
						v-show="isDropdownVisible"
					>
						<a @click="triggerModal" href="#menu-section">MENU COMPLET</a>
					</div>
				</div>

				<a href="#cta-section" class="nav">Contact</a>
			</div>
			<div class="hamburger-menu-container" @click="openMenu">
				<div
					class="hamburger-menu"
					:class="{ close: isActive }"
					id="toggle-menu"
				></div>
			</div>
		</div>

		<div class="nav-mobile">
			<a href="#hero-section" class="mobile-element" @click="openMenu"
				>Accueil</a
			>
			<a href="#about-section" class="mobile-element" @click="openMenu"
				>A propos</a
			>
			<a href="#menu-section" class="mobile-element" @click="openMenu">Menu</a>
			<a href="#cta-section" class="mobile-element" @click="openMenu"
				>Contact</a
			>
		</div>
	</section>
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
