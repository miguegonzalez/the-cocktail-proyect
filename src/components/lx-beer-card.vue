<template>
  <div class="lx-beer-card">
    <div class="cols-auto lx-beer-card__image"><img :src="image_url" /></div>
    <div class="col lx-beer-card__info">
      <div class="row">
        <div class="col">
          <div class="lx-beer-card__name-beer">{{ name_beer }}</div>
          <div class="lx-beer-card__description">{{ description }}</div>
        </div>
      </div>
      <div class="row lx-beer-card__food-pairing">
        <div class="p-medium">
          <span>Ideal para combinar con:&nbsp;</span>
          <span v-for="(item, index) in food_pairing" :key="index">
            <span v-if="index == Object.keys(food_pairing).length - 1" >&nbsp;y </span>
            <span v-else-if="index != 0">, </span>
            <span> {{ item }}</span>
            <span v-if="index == Object.keys(food_pairing).length - 1">.</span>
          </span>
        </div>
      </div>
    </div>
    <div class="cols-auto lx-beer-card__abv" :class="bgAbv()"> {{ abv }}</div>
  </div>
</template>

<script>
export default {
  name: 'lx-beer-card',
  props: {
    image_url: String,
    name_beer: String,
    description: String,
    food_pairing: Array,
    abv: Number,
  },
  methods: {
    bgAbv() {
      var abv_value;
      this.abv <= "5.0" ? abv_value = 'bg-warning' : (this.abv >= "10.0" ? abv_value = 'bg-danger text-white' : abv_value = 'bg-info')
      return abv_value;
    }
  }
}
</script>
