<template>
	<button class="button">
		<slot />
	</button>
</template>

<script>
export default {};
</script>

<style lang="scss">
.button {
	font-family: Open Sans;
	font-weight: bold;
	font-size: 1vw;
	text-transform: uppercase;

	width: 15vw;
	height: 4vw;

	color: white;
	background: #5896fa;

	border: none;
	border-radius: 0.25vw;

	transition: box-shadow 150ms ease-out;

	&:hover {
		box-shadow: 0px 0.3vw 1.2vw rgba(66, 138, 255, 0.42);
	}
}
</style>