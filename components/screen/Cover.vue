<template>
	<div class="cover-screen">
		<div class="cover-screen__bg-video-container">
			<video class="cover-screen__bg-video" autoplay muted loop>
				<source src="~assets/video/background.mp4" type="video/mp4" />
			</video>
			<div class="cover-screen__bg-video-container-overlay"></div>
		</div>
		<div class="cover-screen__section">
			<img class="logo cover-screen__logo" src="@/assets/img/logo.png" />
			<h1 class="cover-screen__title" v-html="title"></h1>
		</div>
		<div class="cover-screen__section">
			<Button>Играть сейчас!</Button>
			<SideBorderedText class="cover-screen__go-down-label">
				Крутой
				<b>подарок</b> ждет тебя
				<b>внизу!</b>
			</SideBorderedText>
			<MouseScrollIcon></MouseScrollIcon>
		</div>
	</div>
</template>

<script>
export default {
	props: {
		title: String,
		background: String,
	},
};
</script>

<style lang="scss">
.cover-screen {
	display: flex;

	flex-flow: column nowrap;
	align-items: center;
	justify-content: space-between;

	height: 100vh;
	padding: 1vw 0;
	box-sizing: border-box;

	position: relative;
	z-index: 20;
	box-shadow: 0 0.5vw 5vw rgba(0, 0, 0, 0.5);
}

.cover-screen__bg-video-container {
	position: absolute;
	z-index: -1;

	width: 100%;
	height: 100%;

	left: 0;
	top: 0;
}
.cover-screen__bg-video {
	width: 100%;
	height: 100%;
	object-fit: cover;
}
.cover-screen__bg-video-container-overlay {
	position: absolute;

	width: 100%;
	height: 100%;
	left: 0;
	top: 0;

	background-color: rgba(0, 0, 0, 0.65);
}

.cover-screen__section {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1vw;
}

.cover-screen__logo {
	width: 20vw;
}

.cover-screen__title {
	font-family: Open Sans;
	font-weight: 600;
	font-size: 1vw;
	line-height: 150%;

	text-align: center;

	color: #ffffff;
}

.innovations-container {
	color: white;
	display: flex;
	flex-flow: column nowrap;
	gap: 1.5vw;
}

.innovations-container__row {
	display: flex;
	justify-content: center;
	gap: 1.5vw;

	&:first-child {
		.innovations-container__item-text {
			margin-top: 0.3vw;
		}
	}

	&:last-child {
		.innovations-container__item-text {
			margin-top: -0.7vw;
		}
	}
}

.innovations-container__item {
	background-size: auto 100%;
	background-repeat: no-repeat;

	height: 6vw;
	display: flex;
	flex-flow: column nowrap;
	justify-content: center;

	box-sizing: border-box;
}
.innovations-container__item_position_top-left {
	background-image: url("../../assets/img/top-left-block.svg");
	background-position: right;
	text-align: right;
	padding-right: 2vw;
	width: 20vw;
}
.innovations-container__item_position_top-center {
	background-image: url("../../assets/img/top-center-block.svg");
	background-position: center;
	text-align: center;
	width: 15vw;
}
.innovations-container__item_position_top-right {
	background-image: url("../../assets/img/top-right-block.svg");
	padding-left: 2vw;
	width: 20vw;
}
.innovations-container__item_position_bottom-left {
	background-image: url("../../assets/img/bottom-left-block.svg");
	text-align: right;
	background-position: right;
	padding-right: 2vw;
	width: 20vw;
}
.innovations-container__item_position_bottom-right {
	background-image: url("../../assets/img/bottom-right-block.svg");
	padding-left: 2vw;
	width: 20vw;
}

.innovations-container__item-text {
	font-family: Open Sans;
	font-weight: 600;
	font-size: 1vw;
}
</style>