<template>
	<div class="cover-screen" :style="{backgroundImage: `url(${background})`}">
		<div>
			<h1 class="cover-screen__title" v-html="title"></h1>
			<h2 class="cover-screen__subtitle" v-html="subtitle"></h2>
		</div>
		<div class="cover-screen__innovations-container innovations-container">
			<div class="innovations-container__row">
				<div class="innovations-container__item innovations-container__item_position_top-left">
					<h3 class="innovations-container__item-text">Теперь доступна отыгровка<br> РП голосом</h3>
				</div>
				<div class="innovations-container__item innovations-container__item_position_top-center">
					<h3 class="innovations-container__item-text">Новая PvP активность:<br> сброс груза</h3>
				</div>
				<div class="innovations-container__item innovations-container__item_position_top-right">
					<h3 class="innovations-container__item-text">
						Новые задания:<br> инструменты фракций
					</h3>
				</div>
			</div>
			<div class="innovations-container__row">
				<div class="innovations-container__item innovations-container__item_position_center-left">
					<h3 class="innovations-container__item-text">
						Получай бесплатные кейсы<br> каждый день
					</h3>
				</div>
				<div class="innovations-container__item innovations-container__item_position_center-right">
					<h3 class="innovations-container__item-text">
						В кейсах теперь гарантировано<br> выпадает авто
					</h3>
				</div>
			</div>
			<div class="innovations-container__row">
				<div class="innovations-container__item innovations-container__item_position_bottom">
					<h3 class="innovations-container__item-text">
						Утилизация скинов<br> и авто
					</h3>
				</div>
			</div>
		</div>
		<div class="cover-screen__conclusion">
			<SideBorderedText class="cover-screen__go-down-label">
				остальное зацени
				<b>сам!</b>
			</SideBorderedText>
			<Button>Играть сейчас!</Button>
		</div>
	</div>
</template>

<script>
export default {
	props: {
		title: String,
		subtitle: String,
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
	background: center/cover;

	position: relative;
	z-index: 20;
	box-shadow: 0 0.5vw 5vw rgba(0, 0, 0, 0.5);
}

.cover-screen__logo {
	width: 20vw;
}

.cover-screen__title {
	font-family: Open Sans;
	font-weight: 600;
	font-size: 1.5vw;
	line-height: 150%;

	text-align: center;

	color: #ffffff;
}
.cover-screen__subtitle {
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
	padding-right: 1vw;
	width: 20vw;
}
.innovations-container__item_position_top-center {
	background-image: url("../../assets/img/top-center-block1.svg");
	background-position: center;
  background-size: contain;
	text-align: center;
	width: 20vw;
}
.innovations-container__item_position_top-right {
	background-image: url("../../assets/img/top-right-block.svg");
	padding-left: 1vw;
	width: 20vw;
}
.innovations-container__item_position_center-left {
	background-image: url("../../assets/img/center-left-block.svg");
	text-align: right;
	background-position: right;
	padding-right: 1vw;
	width: 20vw;
}
.innovations-container__item_position_center-right {
	background-image: url("../../assets/img/center-right-block.svg");
	padding-left: 1vw;
	width: 20vw;
}
.innovations-container__item_position_bottom {
	background-image: url("../../assets/img/bottom-block.svg");
	width: 20vw;
  text-align: center;
}

.innovations-container__item-text {
	font-family: Open Sans;
	font-weight: 600;
	font-size: .75vw;
}

.cover-screen__conclusion {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1vw;
}
</style>