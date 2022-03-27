<template>
	<div class="business-screen">
		<div>
			<h2 class="business-screen__title">новые бизнесы</h2>
			<h3
				class="business-screen__subtitle"
			>В игру добавлены 20 новых бизнесов. Теперь собственный бизнес стал еще доступнее</h3>
		</div>
		<BusinessPreview
			class="business-screen__preview"
			:style="{width: '15vw', top: '10vw', left: '10vw'}"
			amount="4"
			:image="require('/assets/img/business/shop.png')"
			title="Продуктовый магазин"
			titleBackgroundColor="#AE3A3A"
			:worthLevel="1"
		></BusinessPreview>
		<BusinessPreview
			class="business-screen__preview"
			:style="{width: '20vw', top: '11.6vw', left: '27vw'}"
			amount="1"
			:image="require('/assets/img/business/sport.png')"
			title="Спортивный комплекс"
			titleBackgroundColor="#D2A73A"
			:worthLevel="3"
		></BusinessPreview>
		<BusinessPreview
			class="business-screen__preview"
			:style="{width: '18vw', top: '10vw', left: '49vw'}"
			amount="1"
			:image="require('/assets/img/business/ship.png')"
			title="Погрузочное судно паллада"
			titleBackgroundColor="#D2A73A"
			:worthLevel="3"
		></BusinessPreview>
		<BusinessPreview
			class="business-screen__preview"
			:style="{width: '16vw', top: '10vw', left: '69vw'}"
			amount="1"
			:image="require('/assets/img/business/stadium.png')"
			title="Стадион Олимпийский"
			titleBackgroundColor="#D2A73A"
			:worthLevel="3"
		></BusinessPreview>
		<BusinessPreview
			class="business-screen__preview"
			:style="{width: '10vw', top: '29vw', left: '8vw'}"
			amount="1"
			:image="require('/assets/img/business/cinema.png')"
			title="Кинотеатр"
			titleBackgroundColor="#82A5DF"
			:worthLevel="2"
		></BusinessPreview>
		<BusinessPreview
			class="business-screen__preview"
			:style="{width: '14vw', top: '29vw', left: '20vw'}"
			amount="2"
			:image="require('/assets/img/business/mall.png')"
			title="ТЦ"
			titleBackgroundColor="#82A5DF"
			:worthLevel="2"
		></BusinessPreview>
		<BusinessPreview
			class="business-screen__preview"
			:style="{width: '12vw', top: '29vw', left: '36vw'}"
			amount="1"
			:image="require('/assets/img/business/hypermarket.png')"
			title="Гипермаркет"
			titleBackgroundColor="#82A5DF"
			:worthLevel="2"
		></BusinessPreview>
		<BusinessPreview
			class="business-screen__preview"
			:style="{width: '15vw', top: '26vw', left: '50vw'}"
			amount="8"
			:image="require('/assets/img/business/shipyard.png')"
			title="Верфь"
			titleBackgroundColor="#82A5DF"
			:worthLevel="2"
		></BusinessPreview>
		<BusinessPreview
			class="business-screen__preview"
			:style="{width: '20vw', top: '27vw', left: '67vw'}"
			amount="1"
			:image="require('/assets/img/business/sawmill.png')"
			title="Лесопилка"
			titleBackgroundColor="#82A5DF"
			:worthLevel="2"
		></BusinessPreview>
		<Button>Играть сейчас!</Button>
	</div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.business-screen {
	display: flex;
	flex-direction: column;
	justify-content: space-between;
	align-items: center;

  position: relative;

	height: 55vw;

	box-sizing: border-box;
	padding-top: 2vw;
	padding-bottom: 6vw;

	font-family: Open Sans;

	background-image: url("~/assets/img/bg-3.png");
	background-position: bottom;
	background-size: cover;
}

.business-screen__title {
	color: white;

	font-size: 1.5vw;
	font-weight: 700;
	text-transform: uppercase;
  text-align: center;

	margin-bottom: 1vw;
}
.business-screen__subtitle {
	color: white;
	font-size: .9vw;
	font-weight: 400;
}
.business-screen__preview {
	position: absolute;
}
</style>