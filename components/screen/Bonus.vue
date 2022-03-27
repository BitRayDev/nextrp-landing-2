<template>
	<div class="bonus-screen">
		<div class="bonus-screen__header">
			<h2 class="bonus-screen__title">{{ title }}</h2>
			<h3 class="bonus-screen__subtitle">{{ subtitle }}</h3>
		</div>
		<div class="bonus-screen__promos">
			<PromocodeReward
				align="left"
        caption="ДЛЯ НОВИЧКОВ"
				:leftImage="require('/assets/img/cash-mountain.png')"
				:rewardFeatures="[
          'Премиум аккаунт на один день',
          'Аптечка',
          'Карточка выхода из тюрьмы',
          'Канистра бензина',
          '30 000 внутриигровой валюты',
        ]"
				highlightColor="#3C4BCF"
				promocode="RBRN10"
			></PromocodeReward>
			<PromocodeReward
				align="right"
        caption="ДЛЯ ВЕРНУВШИХСЯ"
				:leftImage="require('/assets/img/bronze-case.png')"
				:rightImage="require('/assets/img/silver-case.png')"
				:rewardFeatures="[
          'Кейс серебряный х1',
          'Кейс бронзовый х2',
        ]"
				highlightColor="#DD3232" 
				promocode="RETURN1"
			></PromocodeReward>
		</div>

		<div class="bonus-screen__how-to-use how-to-use">
			<div class="how-to-use__instractions" v-if="isHowToUseShown">
				<p>
					<b>01</b> Заходим в игру
				</p>
				<p>
					<b>02</b> Выбираем МАГАЗИН
				</p>
				<p>
					<b>03</b> Ищем поле ввода
				</p>
				<p>
					<b>04</b> Вводим промокод
				</p>
				<p>
					<b>05</b> Вы великолепны!
				</p>
			</div>
			<a class="how-to-use__link" v-else @click="showHowToUse">
				<img class="how-to-use__icon" src="@/assets/img/icons/tap.svg" />
				Где и как вводить промокод?
			</a>
		</div>
		<Button>Играть бесплатно</Button>
	</div>
</template>

<script>
export default {
	props: {
		title: String,
		subtitle: String,
		rewardColor: String,
		leftImage: String,
		rightImage: String,
		rewardFeatures: Array,
		promocode: String,
	},
	data: function () {
		return {
			isHowToUseShown: false,
		};
	},
	methods: {
		showHowToUse: function () {
			this.isHowToUseShown = true;
		},
	},
};
</script>

<style lang="scss">
.bonus-screen {
	display: flex;
	flex-direction: column;
	justify-content: space-between;
	align-items: center;

	font-family: "Open Sans";

	height: 46vw;

	box-sizing: border-box;
	padding: 2vw;

	background: url("~/assets/img/bg-5.png");
	background-size: cover;
	background-position: center;
}

.bonus-screen__header {
	text-align: center;
	color: white;
}

.bonus-screen__title {
	font-size: 1.5vw;
	font-weight: 700;
	text-transform: uppercase;
}
.bonus-screen__subtitle {
	font-size: 0.9vw;
	font-weight: 700;
}

.bonus-screen__promos {
	display: flex;
	gap: 5vw;
}

.how-to-use {
	height: 2vw;
}

.how-to-use__link {
	display: flex;
	align-items: center;
	flex-flow: row nowrap;
	white-space: nowrap;
	gap: 0.5vw;

	font-size: 1vw;

	text-decoration: underline;
	color: white;
}

.how-to-use__icon {
	height: 1.5vw;
}

.how-to-use__instractions {
	font-size: 1vw;
	color: white;

	b {
		font-family: "Oxanium";
		color: #dd3232;
	}
}
</style>