<template>
	<div class="cars-container">
		<div>
			<h2 class="cars-container__title">Обновленный автопарк</h2>
			<h3 class="cars-container__subtitle">
				В игру постоянно добавляются
				<b>новые</b> автомобили
			</h3>
		</div>
		<div class="cars-container__slider-container">
			<Slider :contentLength="cars.length">
				<template v-slot="slotProps">
					<SliderCarsContent  :cars="cars" :currentContentIndex="slotProps.currentContentIndex"></SliderCarsContent>
				</template>
			</Slider>
		</div>
		<Button>Играть сейчас!</Button>
	</div>
</template>

<script>
export default {
	props: {
		cars: {
			type: Array,
			required: true,
		},
	},
};
</script>

<style lang="scss">
.cars-container {
  display: flex;
	flex-direction: column;
	justify-content: space-between;
	align-items: center;

  position: relative;
	height: 55vw;

	box-sizing: border-box;
	padding-top: 2vw;
	padding-bottom: 6vw;

	font-family: Open Sans;

	background: url("~/assets/img/cars-bg.png"), black;
	background-position: bottom;
	background-size: cover;
}

.cars-container__title {
	color: white;

	font-size: 1.5vw;
	font-weight: 700;
	text-transform: uppercase;
  text-align: center;
}
.cars-container__subtitle {
	margin-top: .25vw;

	color: white;

	font-size: .8vw;
	font-weight: 400;
  text-align: center;

	b {
		color: #dd3232;
	}
}

.cars-container__slider-container {
	width: 55vw;
  height: 27vw;
}
</style>