<template>
	<div class="game-system">
		<div class="game-system__content">
			<div class="game-system__title-and-slider">
				<div class="game-system__text">
					<h3 class="game-system__title">{{ title }}</h3>
					<h3 class="game-system__subtitle">{{ subtitle }}</h3>
				</div>
				<div class="game-system__slider-container">
					<Slider :contentLength="sliderImages.length">
						<template v-slot="slotProps">
							<SliderImageContent
								:images="sliderImages"
								:currentContentIndex="slotProps.currentContentIndex"
							></SliderImageContent>
						</template>
					</Slider>
				</div>
			</div>
			<div class="game-system__list-and-prize">
				<ul class="game-system__list">
					<li
						class="game-system__list-item"
						v-for="(item, index) in listItems"
						:key="index"
						v-html="item"
					></li>
				</ul>
				<div class="game-system__prize">
					<p class="game-system__prize-title">Главный приз</p>
					<img class="game-system__prize-image" src="~assets/img/rotating-car.gif" />
				</div>
			</div>
		</div>
		<Button>Играть сейчас</Button>
	</div>
</template>

<script>
export default {
	props: {
		title: String,
		subtitle: String,
		listItems: Array,
		sliderImages: Array,
	},
};
</script>

<style lang="scss">
.game-system {
	display: flex;
	flex-flow: column nowrap;
	justify-content: space-between;
	align-items: center;
	gap: 2vw;

	font-family: Open Sans;

	background-image: url("../../assets/img/bg-1.png");
	background-size: cover;
	background-position: center;

	box-sizing: border-box;
	padding: 4vw;
}

.game-system__content {
	display: flex;
	flex-flow: row;
	gap: 5vw;

	width: 70vw;
}

.game-system__title-and-slider {
	display: flex;
	flex-direction: column;
	justify-content: space-between;

	height: 27vw;
}

.game-system__text {
	margin-bottom: 4.5vw;

	color: white;
}
.game-system__title {
	font-weight: 700;
	font-size: 1.5vw;
	text-transform: uppercase;
	border: 0 solid #dd3232;
	border-width: 0 0 0.4vw 0;
	padding-bottom: 0.5vw;
	margin-bottom: 0.5vw;
}
.game-system__subtitle {
	font-weight: 600;
	font-size: 0.9vw;
}

.game-system__slider-container {
	width: 35vw;
	height: 20vw;
	flex-shrink: 0;
}

.game-system__list {
	margin-top: 4vw;

  list-style: none;

	color: white;
}
.game-system__list-item {
	margin-bottom: 1.1vw;
	padding-left: 0.25vw;

	font-size: 0.8vw;
	font-weight: 700;

	&::marker {
		content: "▸";
	}

	b {
		color: #5896fa;
	}
}

.game-system__prize {
	width: fit-content;

	margin-top: 3vw;

	background-color: #d2a73a;
}
.game-system__prize-title {
	font-size: 1vw;
	font-weight: 700;

	text-transform: uppercase;

	padding: 0.25vw 0.5vw;

	color: white;
}
.game-system__prize-image {
	width: 25vw;
	height: 11vw;

	object-fit: cover;
	object-position: top;
}
</style>