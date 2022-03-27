<template>
	<div class="slider-container">
		<div class="slider-container__image-container">
			<div class="slider-container__button-container">
				<img
					class="slider-container__button slider-container__button_type_prev"
					src="@/assets/img/icons/arrow.svg"
					@click="showPrevious"
				/>
			</div>
			<slot :currentContentIndex="currentContentIndex"></slot>
			<div class="slider-container__button-container">
				<img
					class="slider-container__button slider-container__button_type_next"
					src="@/assets/img/icons/arrow.svg"
					@click="showNext"
				/>
			</div>
		</div>
		<div class="slider-container__points">
			<div
				v-for="(value, index) in contentLength"
				class="slider-container__point"
				:class="{
          'slider-container__point_active': currentContentIndex == index,
        }"
				:key="index"
			/>
		</div>
	</div>
</template>

<script>
export default {
	props: {
		contentLength: {
			type: Number,
			required: true,
		},
	},
	data: function () {
		return {
			currentContentIndex: 0,
		};
	},
	methods: {
		showPrevious: function () {
			this.currentContentIndex--;
			if (this.currentContentIndex < 0)
				this.currentContentIndex = this.contentLength - 1;
		},
		showNext: function () {
			this.currentContentIndex++;
			if (this.currentContentIndex >= this.contentLength)
				this.currentContentIndex = 0;
		},
	},
};
</script>

<style lang="scss">
.slider-container {
	display: flex;
	flex-flow: column nowrap;
	gap: 0.75vw;

	width: 100%;
	min-height: 20vw;
	height: 100%;
}

.slider-container__image-container {
	display: flex;
	align-items: center;
	justify-content: space-between;
	gap: 1vw;

	flex-grow: 1;
}
.slider-container__image {
	height: 100%;
}

.slider-container__button-container {
  position: relative;
  z-index: 1;

	width: 1.1vw;
	flex-shrink: 0;
}
.slider-container__button {
	transition: width 100ms ease-in;
	width: 1vw;

	&:hover {
		width: 1.1vw;
	}
}
.slider-container__button_type_next {
	transform: scaleX(-1);
}

.slider-container__points {
	display: flex;
	justify-content: center;
	gap: 0.5vw;
}
.slider-container__point {
	width: 0.5vw;
	height: 0.5vw;

	border-radius: 100vw;
	background-color: #8c8c8c;
}
.slider-container__point_active {
	background-color: #3c4bcf;
}
</style>