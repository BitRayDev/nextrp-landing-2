<template>
	<div class="step-block-container">
		<span v-html="text"></span>
		<div class="step-block-container__index-container">{{index}}</div>
	</div>
</template>

<script>
export default {
	props: {
		text: {
			type: String,
			required: true,
		},
		index: {
			type: Number,
			required: true,
		},
	},
};
</script>

<style lang="scss">
.step-block-container {
	color: white;

	font-size: 0.9vw;
	font-family: Open Sans;
	font-weight: 600;

	background: #272b31;
	border: 2px solid #606060;

	padding: 1vw 2vw;
	box-sizing: border-box;
	position: relative;
}

.step-block-container__index-container {
	display: flex;
	justify-content: center;
	align-items: center;

	font-family: "Oxanium";
	font-weight: 700;
	font-size: 1.5vw;

	position: absolute;
	right: -2.5vw;
	top: 50%;
	transform: translate(-50%, -50%);

	height: 3vw;
	width: 3vw;

	border-radius: 0.5vw;
	background-color: #7aadff;
	box-shadow: 0px 4px 13px rgba(66, 138, 255, 0.25);
}

.step-block-container b {
	color: #dd3232;
}
</style>