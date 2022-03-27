<template>
	<div class="slider-case-content" :key="currentContentIndex">
		<h3 class="slider-case-content__name">«{{cases[currentContentIndex].name}}»</h3>
		<img class="slider-case-content__case-image" :src="cases[currentContentIndex].caseImage" />
		<img class="slider-case-content__cars-image" :src="cases[currentContentIndex].carsImage" />
	</div>
</template>

<script>
export default {
	props: {
		cases: {
			type: Array,
			required: true,
		},
		currentContentIndex: Number,
	},
};
</script>

<style>
.slider-case-content {
	width: 100%;
	height: 20vw;

	font-family: Open Sans;

	position: relative;
}
.slider-case-content__name {
	color: white;

	font-size: 1.5vw;
	text-align: center;
	text-transform: uppercase;

	margin-bottom: 1vw;
}
.slider-case-content__case-image {
	height: 20vw;
	position: absolute;
	left: 0;
	z-index: 2;
}
.slider-case-content__cars-image {
	height: 16vw;
	position: absolute;
	right: 0;
}
</style>