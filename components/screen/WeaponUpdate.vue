<template>
	<div class="weapon-container">
		<div class="weapon-container__text">
			<h4 class="weapon-container__subtitle">НОВАЯ СИСТЕМА ОРУЖИЯ</h4>
			<h3 class="weapon-container__title">"ОРУЖИЕ 2.0"</h3>
		</div>
		<div class="weapon-container__content">
			<div class="weapon-features">
				<BlockWithIcon :icon="require('~/assets/img/icons/gear-wheel.png')">
					<div class="weapon-feature">
						Полная переработка внешнего вида
						и механик
					</div>
				</BlockWithIcon>
				<BlockWithIcon :icon="require('~/assets/img/icons/new.png')">
					<div class="weapon-feature">
						<p>Новые модели оружия</p>
						<div class="weapon-feature__splitter" />
						<table class="weapon-models">
							<tr>
								<td>NOVA</td>
								<td>SPAS-12</td>
							</tr>
							<tr>
								<td>Uzi</td>
								<td>Vector</td>
							</tr>
							<tr>
								<td>AR15</td>
								<td>ТОЗ-119</td>
							</tr>
						</table>
						<div class="weapon-feature__splitter" />
						<p>и многие другие</p>
					</div>
				</BlockWithIcon>
				<BlockWithIcon :icon="require('~/assets/img/icons/instruments.png')">
					<div class="weapon-feature">
						Добавлен износ оружия
						и возможность
						ремонта
					</div>
				</BlockWithIcon>
			</div>
			<div class="weapon-container__video-container">
				<h3 class="weapon-container__video-container-title">улучшение и модификация ОРУЖИЯ</h3>
				<video class="weapon-container__video-container-video" autoplay muted loop>
					<source src="@/assets/video/guns.mp4" type="video/mp4" />
				</video>
			</div>
		</div>
    <Button>Играть сейчас</Button>
	</div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.weapon-container {
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	gap: 2vw;

	font-family: Open Sans;

	background: url("../../assets/img/weapons-bg.png"), black;
	background-size: cover;

	padding: 3vw 0;

	position: relative;
	z-index: 19;
	box-shadow: 0 0.5vw 5vw rgba(0, 0, 0, 0.9);
}

.weapon-container__text {
	font-weight: bold;
	text-align: center;
	color: white;
}
.weapon-container__subtitle {
	font-size: 1vw;
}
.weapon-container__title {
	font-size: 1.5vw;
}

.weapon-container__content {
	display: flex;
  gap: 1.5vw;

  margin: 4vw 0;
}

.weapon-features {
	display: flex;
	flex-direction: column;
	gap: 2vw;

	font-size: 1vw;

	color: white;
}

.weapon-feature {
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;

	width: 13vw;
	text-align: center;
}

.weapon-feature__splitter {
	background-color: white;
	height: .1vw;
	width: 50%;
	margin: .25vw 0;
}
.weapon-models {
	width: 80%;
	font-family: Open Sans;
	font-weight: 400;
	font-size: 0.85vw;
}


.weapon-container__video-container {
	display: flex;
	flex-direction: column;
	align-items: flex-end;
}
.weapon-container__video-container-title {
	font-size: 1vw;
	font-weight: 700;
	text-transform: uppercase;
	text-align: center;

	color: white;

	width: 22vw;

	border: solid #dd3232;
	border-width: 0 0 0.4vw 0;

	padding-bottom: 0.5vw;
	margin-bottom: 1vw;
}
.weapon-container__video-container-video {
	width: 38vw;
}
</style>