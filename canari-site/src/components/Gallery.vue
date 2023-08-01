<template>
	<div class="gallery-container">
		<swiper
			:modules="modules"
			:slides-per-view="3"
			:space-between="0"
			navigation
			:pagination="{ clickable: true }"
			:scrollbar="{ draggable: true }"
			:breakpoints="{
				'950': {
					slidesPerView: 3,
					spaceBetween: 0,
				},
				'0': {
					slidesPerView: 1,
					spaceBetween: 5,
				},
			}"
			@swiper="onSwiper"
			@slideChange="onSlideChange"
		>
			<swiper-slide
				><img
					class="gallery-img"
					src="../assets/thumbnail_image001.jpg"
					loading="lazy"
					alt="Intérieur accueillant du restaurant Canari"
			/></swiper-slide>
			<swiper-slide>
				<video
					class="gallery-img gallery-video"
					autoplay
					muted
					playsinline
					loop
				>
					<source
						src="../assets/video-main.mp4"
						type="video/mp4"
						loading="lazy"
					/>
				</video>
			</swiper-slide>
			<swiper-slide
				><img
					class="gallery-img"
					src="../assets/thumbnail_image003.jpg"
					loading="lazy"
					alt="Elegant dining au restaurant Canari"
			/></swiper-slide>
			<swiper-slide
				><img
					class="gallery-img"
					src="../assets/thumbnail_image004.jpg"
					loading="lazy"
					alt="Peinture trouvée à l'intérieur du restaurant Canari"
			/></swiper-slide>

			...
		</swiper>
	</div>
</template>
<script>
// import Swiper core and required modules
import { Navigation, Pagination, Scrollbar, A11y } from "swiper/modules";

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

// Import Swiper styles
export default {
	components: {
		Swiper,
		SwiperSlide,
	},
	setup() {
		const onSwiper = swiper => {
			console.log(swiper);
		};
		const onSlideChange = () => {
			console.log("slide change");
		};
		return {
			onSwiper,
			onSlideChange,
			modules: [Navigation, Pagination, Scrollbar, A11y],
		};
	},
};
</script>

<style scoped>
@import "../style.css";
</style>
