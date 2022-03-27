<template>
	<div>
	  <p class="promocode-reward-caption" :style="{textAlign: align}">{{caption}}</p>
  	<div class="promocode-reward-container">
  		<div
  			class="promocode-reward-container__color-border"
  			:style="{backgroundColor: highlightColor, right: align == 'right' ? '0' : 'auto'}"
  		></div>
  		<div class="promocode-reward">
  			<div class="promocode-reward__section promocode-reward__section_type_promocode">
  				<h3 class="promocode-reward__section-title">Промокод</h3>
  				<h3 class="promocode-reward__promocode" :style="{borderColor: highlightColor}">{{promocode}}</h3>
  			</div>
  			<div class="promocode-reward__section">
  				<h3 class="promocode-reward__section-title">Награда</h3>
  				<ul class="promocode-reward__reward-features">
  					<li class="promocode-reward__reward-feature" v-for="feature in rewardFeatures">{{feature}}</li>
  				</ul>
  				<img
  					class="promocode-reward__image promocode-reward__image_position_left"
  					:src="leftImage"
  					:style="{
  	          filter: `drop-shadow(0 0 2.5vw ${highlightColor}AA)` 
            }"
  				/>
  				<img
  					class="promocode-reward__image promocode-reward__image_position_right"
  					:src="rightImage"
  					:style="{
  	          filter: `drop-shadow(0 0 2.5vw ${highlightColor}AA)` 
            }"
  				/>
  			</div>
  		</div>
  	</div>
	</div>
</template>

<script>
export default {
	props: {
		align: {
      type: String,
      default: "left"
    },
		caption: String,
		promocode: String,
		rewardFeatures: Array,
		leftImage: String,
		rightImage: String,
		highlightColor: String,
	},
};
</script>

<style lang="scss">
.promocode-reward-caption {
  margin-bottom: .6vw;

  font-size: 1vw;
  font-weight: 700;

  color: white;
}
.promocode-reward-container {
	position: relative;
}

.promocode-reward-container__color-border {
	position: absolute;
	top: -0.35vw;

	width: 12vw;
	height: 5vw;

	z-index: 0;
}

.promocode-reward {
	display: flex;
	justify-content: space-between;
	color: white;

	font-weight: 600;

	width: 28vw;
	height: 16vw;

	position: relative;
	background-color: #171717;

	z-index: 1;
}

.promocode-reward__section {
	padding: 1vw 1.5vw;
}
.promocode-reward__section_type_promocode {
}

.promocode-reward__section-title {
	font-size: 1.1vw;
	font-weight: 600;

	margin-bottom: 0.5vw;
}

.promocode-reward__promocode {
	font-size: 1.1vw;
	text-align: center;

	width: 6vw;
	padding: 0.5vw 0.25vw;
	border: 0.14vw dashed white;
}

.promocode-reward__reward-feature {
  margin-top: .5vw;
  padding-left: 0.25vw;

	font-size: 0.9vw;

  &::marker {
    content: "▸";
  }
}

.promocode-reward__image {
	position: absolute;
}
.promocode-reward__image_position_left {
	bottom: -1vw;
	left: 0;

	transform: translate(-35%, 25%);
	height: 12vw;
}
.promocode-reward__image_position_right {
	bottom: -3vw;
	right: 0;

	transform: translate(35%, 25%);
	height: 16vw;
}
</style>