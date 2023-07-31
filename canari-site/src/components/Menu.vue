<template>
	<!-- menu section -->
	<section class="menu-container" id="menu-section">
		<div class="menu-box">
			<div class="sauces">
				<h2 class="menu-title">NOS SAUCES (3000 CFA)</h2>
				<div class="menu-item">
					<p class="item-title">Sauce Gombo (Kopè)</p>
					<p class="item-description">
						Traditionnelle, savoureux mélange d'okra, viande tendre et épices
						africaines
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Sauce Arachide</p>
					<p class="item-description">
						Savoureuse sauce Arachide riche en cacahuètes et parfumée aux
						épices, une délicieuse touche africaine pleine de saveurs.
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Sauce Graine</p>
					<p class="item-description">
						A base de graines de palme et d'épices locales
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Sauce Feuille</p>
					<p class="item-description">
						Préparée avec des feuilles fraîches et un assortiment d'épices, une
						symphonie de saveurs végétales.
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Sauce Tomate Cocktail</p>
					<p class="item-description">
						Un mélange exquis de tomates fraîches et d'herbes, rehaussant
						délicieusement tous les plats.
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Sauce Claire Poisson Frais</p>
					<p class="item-description">
						Légère et parfumée, sublimant la fraîcheur des poissons avec une
						touche de saveurs raffinées.
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Sauce Gouagouassou</p>
					<p class="item-description">
						Un délice ivoirien épicé à base de piments, tomates et épices
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Sauce Claire Gingembre Cabri</p>
					<p class="item-description">
						Une fusion équilibrée de gingembre, viande tendre et épices, pour
						une expérience culinaire ivoirienne unique.
					</p>
				</div>
				<div class="menu-item">
					<p class="item-title">Sauce Egusi</p>
					<p class="item-description">
						Un trésor africain aux graines de courge, arachides et épices
					</p>
				</div>
			</div>
			<a class="btn btn-menu" @click="showModal">VOIR MENU COMPLET</a>

			<!-- MODAL -->
			<div
				:class="{ 'modal-background': modalVisible }"
				@click="closeModal"
			></div>
			<modal id="modal" class="modal" :visible="modalVisible">
				<div class="modal-close-container" @click="closeModal">
					<div class="modal-close"></div>
				</div>
				<h2 class="modal-title">DISPONIBLE TOUS LES JOURS DE LA SEMAINE</h2>
				<div class="modal-menu">
					<!-- SAUCES -->
					<div class="sauces">
						<h2 class="menu-title">NOS SAUCES (3000 CFA)</h2>
						<div class="menu-item">
							<p class="item-title">Sauce Gombo (Kopè)</p>
							<p class="item-description">
								Traditionnelle, savoureux mélange d'okra, viande tendre et
								épices africaines
							</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Sauce Arachide</p>
							<p class="item-description">
								Savoureuse sauce Arachide riche en cacahuètes et parfumée aux
								épices, une délicieuse touche africaine pleine de saveurs.
							</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Sauce Graine</p>
							<p class="item-description">
								A base de graines de palme et d'épices locales
							</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Sauce Feuille</p>
							<p class="item-description">
								Préparée avec des feuilles fraîches et un assortiment d'épices,
								une symphonie de saveurs végétales.
							</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Sauce Tomate Cocktail</p>
							<p class="item-description">
								Un mélange exquis de tomates fraîches et d'herbes, rehaussant
								délicieusement tous les plats.
							</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Sauce Claire Poisson Frais</p>
							<p class="item-description">
								Légère et parfumée, sublimant la fraîcheur des poissons avec une
								touche de saveurs raffinées.
							</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Sauce Gouagouassou</p>
							<p class="item-description">
								Un délice ivoirien épicé à base de piments, tomates et épices
							</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Sauce Claire Gingembre Cabri</p>
							<p class="item-description">
								Une fusion équilibrée de gingembre, viande tendre et épices,
								pour une expérience culinaire ivoirienne unique.
							</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Sauce Egusi</p>
							<p class="item-description">
								Un trésor africain aux graines de courge, arachides et épices
							</p>
						</div>
					</div>
					<!-- ACCOMPAGNEMENTS -->
					<div class="sides">
						<h2 class="menu-title">NOS ACCOMPAGNEMENTS (1000 CFA)</h2>
						<div class="menu-item">
							<p class="item-title">Foutou</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Foufou</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Placali</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Akassa</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Kabato</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Riz</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Attieke</p>
							<p class="item-subtitle">blanc ou rouge</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Frite</p>
							<p class="item-subtitle">Pomme de terre, Ignam ou patate douce</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Alloco</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Banane bouillie</p>
						</div>
						<div class="menu-item">
							<p class="item-title">Ignam bouillie</p>
						</div>
					</div>
				</div>
			</modal>
		</div>
	</section>
	<!-- menu section -->
</template>

<script>
import Modal from "./Modal.vue";

export default {
	name: "Menu",
	props: {
		showModal: Boolean,
	},
	components: {
		Modal,
	},
	data() {
		return {
			modalVisible: false,
		};
	},
	methods: {
		showModal() {
			this.modalVisible = true;
		},
		closeModal() {
			this.modalVisible = false;
		},
	},
};
</script>
<style scoped>
@import "../style.css";
</style>
