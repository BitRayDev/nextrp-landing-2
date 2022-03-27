<template>
	<div>
		<ScreenCover
			title="Встречай Королевскую Битву!<br>Самое масштабное и захватывающее событие"
		></ScreenCover>
		<ScreenGameSystem
			:title="battleRoyal.title"
			:subtitle="battleRoyal.subtitle"
			:listItems="battleRoyal.listItems"
			:sliderImages="battleRoyal.sliderImages"
		></ScreenGameSystem>
		<ScreenWeaponUpdate></ScreenWeaponUpdate>
    <ScreenBusiness></ScreenBusiness>
		<ScreenCars :cars="cars"></ScreenCars>
    <ScreenCover2
			:background="require('@/assets/img/cover-2-bg.png')"
			title="Другие изменения"
      subtitle="Во <b>фракциях</b>, <b>кланах</b> и не только. Новые <b>задания</b>, <b>награды</b> и <b>возможности</b>"
		></ScreenCover2>
		<ScreenBonus
			title="забирай свой бонус"
			subtitle="Врывайся в игру прямо сейчас и получай вкусные ништяки!"
		></ScreenBonus>
		<Footer></Footer>
	</div>
</template>

<script>
import screenshot1 from "~/assets/img/screenshots/1.png";
import screenshot2 from "~/assets/img/screenshots/2.png";
import screenshot3 from "~/assets/img/screenshots/3.png";
import screenshot4 from "~/assets/img/screenshots/4.png";
import screenshot5 from "~/assets/img/screenshots/5.png";
import screenshot6 from "~/assets/img/screenshots/6.png";
import screenshot7 from "~/assets/img/screenshots/7.png";

import car1 from "~/assets/img/cars/1.png";
import car2 from "~/assets/img/cars/2.png";
import car3 from "~/assets/img/cars/3.png";
import car4 from "~/assets/img/cars/4.png";
import car5 from "~/assets/img/cars/5.png";
import car6 from "~/assets/img/cars/6.png";
import car7 from "~/assets/img/cars/7.png";
import car8 from "~/assets/img/cars/8.png";
import car9 from "~/assets/img/cars/9.png";

export default {
	data: function () {
		return {
			cars: [
				car1,
        car2,
        car3,
        car4,
        car5,
        car6,
        car7,
        car8,
        car9,
			],
			battleRoyal: {
				title: "Встречай Королевскую Битву!",
				subtitle: "Самое масштабное и захватывающее событие!",
				listItems: [
          'Участвуют <b>10</b> команд по <b>2</b> человека. Так что время звать друзей!',
          'Выбирай подходящее <b>оружие</b> и десантируйся с парашютом на поле боя',
          '<b>Модифицируй</b> свое оружие, чтобы стать сильнее',
          '<b>Сокрушай</b> вражеские команды, чтобы победить',
          'На карте разбросаны различные <b>бонусы</b> в виде аптечек и брони, используй их!',
          'Победит команда, которая останется <b>последней</b>!',
        ],
				sliderImages: [
					screenshot1,
					screenshot2,
					screenshot3,
					screenshot4,
					screenshot5,
				],
			},
		};
	},
};
</script>

<style>
</style>