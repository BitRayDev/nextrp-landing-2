<template>
	<h2 class="side-bordered-text">
		<slot />
	</h2>
</template>

<script>
export default {};
</script>

<style lang="scss">
.side-bordered-text {
	font-family: Open Sans;
	font-weight: 600;
	font-size: 1vw;

	text-align: center;
	text-transform: uppercase;

	color: white;

	border: solid #dd3232;
	border-width: 0 0.5vw;

	padding: 0.5vw 1vw;
}

.side-bordered-text b {
	color: #dd3232;
}
</style>