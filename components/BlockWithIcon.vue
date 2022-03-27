<template>
	<div class="block-container">
		<div class="block-container__icon-container">
			<img class="block-container__icon" :src="icon" />
		</div>
		<slot></slot>
	</div>
</template>

<script>
export default {
	props: {
		icon: String,
	},
};
</script>

<style lang="scss">
.block-container {
	position: relative;

	box-sizing: border-box;
  padding: 1vw 2vw;
  padding-left: 3vw;

	background: #171717;
	border: 2px solid #606060;
}

.block-container__icon-container {
	display: flex;
	justify-content: center;
	align-items: center;

	position: absolute;
	height: 6vw;
	width: 6vw;
	left: -3.5vw;
	top: 50%;
  transform: translateY(-50%);

	background-color: #dd3232;
	border-radius: 20vw;
	box-shadow: 0px 4px 13px rgba(221, 50, 50, 0.5);
}
.block-container__icon {
	width: 60%;
	max-height: 60%;
}
</style>