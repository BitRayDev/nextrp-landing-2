<template>
  <div class="business-preview">
    <p class="business-preview__amount">x{{amount}}</p>
    <img class="business-preview__image" :src="image"/>
    <p class="business-preview__title" :style="{backgroundColor: titleBackgroundColor}">{{title}}</p>
    <div class="business-preview__dollars-container">
      <span v-for="index in 3" :style="{color: index <= worthLevel ? 'white' : '#616E84'}">$</span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    image: String,
    amount: Number,
    titleBackgroundColor: String,
    worthLevel: Number,
  }
}
</script>

<style lang="scss">
.business-preview {
  background-color: #313844;
  border: .2vw solid #ADADAD;
}
.business-preview__amount {
  position: absolute;

  padding: .25vw .5vw;

  font-size: 1.2vw;
  font-weight: 900;

  color: white;
  background-color: #606060;
}
.business-preview__image {
  display: block;

  width: 100%;
}
.business-preview__title {
  padding: .25vw .5vw;

  font-size: .9vw;
  font-weight: 600;

  color: white;
  background-color: #606060;

  border: solid #ADADAD;
  border-width: 0 0 .2vw 0;
}
.business-preview__dollars-container {
  padding: .25vw .5vw;

  font-size: .9vw;
  font-weight: 600;

  color: white;
}
</style>