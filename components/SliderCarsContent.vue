<template>
	<transition name="component-fade" mode="out-in">
		<div class="slider-cars__content">
			<div
				class="slider-cars__car-container"
				v-for="(car, index) in cars"
				:key="index"
        :style="{transform: `translateX(-${100*currentContentIndex}%)`}"
			>
				<img class="slider-cars__car" :src="car" />
			</div>
		</div>
	</transition>
</template>

<script>
export default {
	props: {
		cars: {
			type: Array,
			required: true,
		},
		currentContentIndex: Number,
	},
};
</script>

<style>
.slider-cars__content {
  display: flex;
  position: absolute;
  left: 0;
  top: 12vw;
  z-index: 0;

  width: 100%;

  overflow: hidden;
}
.slider-cars__car-container {
  position: relative;
  flex-shrink: 0;

	width: 100%;
  height: 25vw;

  transition: transform 300ms ease-out;
}
.slider-cars__car {
	width: 40%;

  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.component-fade-enter-active,
.component-fade-leave-active {
	transition: opacity 0.3s ease;
}
.component-fade-enter-from,
.component-fade-leave-to {
	opacity: 0;
}
</style>