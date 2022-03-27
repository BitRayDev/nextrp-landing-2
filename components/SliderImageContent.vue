<template>
	<transition name="component-fade" mode="out-in">
		<div class="slider__content">
			<div
				class="slider__image-container"
				v-for="(image, index) in images"
				:key="index"
        :style="{transform: `translateX(-${100*currentContentIndex}%)`}"
			>
				<img class="slider__image" :src="image" />
			</div>
		</div>
	</transition>
</template>

<script>
export default {
	props: {
		images: {
			type: Array,
			required: true,
		},
		currentContentIndex: Number,
	},
};
</script>

<style>
.slider__content {
  display: flex;

  width: 90%;

  overflow: hidden;
}
.slider__image-container {
  flex-shrink: 0;

	width: 100%;

  transition: transform 300ms ease-out;
}
.slider__image {
	width: 100%;
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